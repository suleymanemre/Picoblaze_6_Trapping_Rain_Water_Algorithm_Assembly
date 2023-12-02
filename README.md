# Picoblaze_6_Trapping_Rain_Water_Algorithm_Assembly
Picoblaze_6_Trapping_Rain_Water_Algorithm_Assembly

Problem Description:
The problem involves iterating through the array of heights and, for each position, calculating the amount of water that can be trapped above that position. The trapped water at each position is determined by the minimum of the maximum heights on the left and right minus the height at the current position.
 
Algorithm:
	To solve that problem there exist two significant solution method one of them is known algorithm.
	Known algorithm takes the first and the last index height. Compare both and uses the least one because least one borders the minimum border of water height.

![1](https://github.com/suleymanemre/Picoblaze_6_Trapping_Rain_Water_Algorithm_Assembly/assets/40830463/eba4ff64-9ba1-4cb0-addc-df437b1a97a5)

 
In the example given above, the length of the last index on the right is 4, and the length of the final index is 5. Here, according to the algorithm, the limit is set as 4, and the assumption is made that the height of the water cannot be less than 4. The algorithm starts by traversing the indices, and the difference between them is calculated.
For example:
•	For the first index: 4 - 2 = 2 units of water are said to be held.
•	For the second index: 4 - 0 = 4 units of water are said to be held.
•	For the third index: 1 unit.
•	For the fourth index: 2 units.
•	For the last index, no calculation is made because water cannot be held.
However, the given algorithm has a problem. If the array is given as shown below, it operates using the system's edge blocks and cannot detect the middle part. Since I couldn't find a short solution to solve this in assembly format, I decided to change the algorithm.
 	 	 	 	 	 	 
![2](https://github.com/suleymanemre/Picoblaze_6_Trapping_Rain_Water_Algorithm_Assembly/assets/40830463/29f6ff3a-12a7-4a41-ba28-a6342487e885)
	 

The algorithm I will use can be defined as follows: I will start from the bottom left corner of the given two-dimensional checkered board and move to the right. At the end of each row, I will move to the next row. While moving along the row, if I see a filled square, I will activate the counter and check the square next to it. If the square next to it is empty (in a condition to hold water), I will increase the counter and check the next square. If, while moving to the right within the row, I encounter a second filled square, it will be certain that water is held, and I will add the counter I held to the total number of blocks holding water. At the same time, at the end of each row, I will reset the counter so that it does not perceive a filled block in the upper row as in the lower row. With this algorithm, the problem of the general algorithm above is solved, and the output is obtained without missing any gaps. I also think that this algorithm is more suitable for modeling in assembly format. It provides a straightforward calculation without the need for finding or changing any maximum. As a drawback, it requires providing input suitable for the array width, as it is not a code that behaves parametrically. Since the growth curve of the code is linear as the array width increases, I think it is a reasonable choice.

![3](https://github.com/suleymanemre/Picoblaze_6_Trapping_Rain_Water_Algorithm_Assembly/assets/40830463/09cd338b-40e0-4cc7-8de6-fa71ef43e02a)

