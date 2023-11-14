# Assignment 5 Write up

Assignment 5 can be broken up into the following parts:
1. Import the Necessary Modules:
- `copy`: For creating deep copies of objects
- `Stack` and `Queue`: Custom implementations for DFS and BFS operations
2. Utility Functions: 
- `remove_if_exists`: Removes a specified element from a list if it exists, which is used to remove the possibilites from a cell
3. Board Class:
- Represents the Sudoku board
- Consists of functions that will find the most constrained cell, and update the board, which eliminates possible solutions
4. DFS & BFS Functions:
- `DFS`: Uses depth-first search to solve the Sudoku puzzle. It works by trying to fill the most constrained cell with potential values until a solution is found or backtracks if a mistake is made
- `BFS`: Uses breadth-first search to solve the Sudoku puzzle in a similar fashion to DFS but explores nodes level by level
5. Main Execution:
- Defines two different sets of initial moves for Sudoku puzzles
- Uses both DFS and BFS to solve each puzzle and prints the results


After completing the assignment, answer the following reflection questions:

## Reflection Questions

1. How do the performance and efficiency of the Depth-First Search (DFS) and Breadth-First Search (BFS) algorithms compare when solving Sudoku puzzles? In what scenarios might one approach be preferable over the other?
The efficiency of each algorithm depends on each Board scenario because what if the DFS algorithm chooses the best value for each square on its first attempt? Technically, it would run faster than the BFS because it would only loop through a singular tree. However, that is rarely the case, which is why I believe BFS is the better option in general because it covers more of a broader ground on each depth loop. It does not tunnel vision on a singular tree that might not even be a solution and it considers every solution before moving on. Yeah, algorithms don't actually 'consider' solutions, but I like to think of them as someone's thought process, so that is my way of comparing the Sudoku algorithms.


2. How did the choice of data structures (like the Stack for DFS and Queue for BFS) impact the implementation and functionality of the algorithms? Are there alternative data structures or design patterns that could have been used to achieve the same objectives?
The data structure determines the order of the loop that the computer runs through each scenario. For DFS, it uses a stack which uses the FILO (first in last out) method while BFS uses a queue which uses the FIFO (first in first out) method. You can also use a general Python list to loop through as stacks and queues are just modified forms of a list.


3. Considering the current implementation, how might the Sudoku solver be adapted or extended for larger puzzles or different types of grid-based logic games? How can the lessons learned from this assignment be applied to real-world problem-solving or optimization challenges?
Luckily, the code we have currently implemented for Sudoku could be reused because not many lines have hardcoded values for the 9x9 grid. We have a self.size property for the length of the board which can easily be editable. One thing that might be a bit tricky would be the modification of subgrid_coordinates because that is generally specific to a 9x9 grid, but it is doable. A takeaway is that there are many ways to solve problems and trying more than one is a good practice for finding the most optimized solution.

