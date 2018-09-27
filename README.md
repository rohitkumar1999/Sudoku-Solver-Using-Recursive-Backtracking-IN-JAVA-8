# Sudoku-Solver-Using-Recursive-Backtracking-IN-JAVA-8
Sudoku  is a logic-based combinatorial number-placement puzzle. Given a partially filled 9×9 2D array grid[9][9], the goal is to assign digits (from 1 to 9) to the empty cells so that every row, column, and subgrid of size 3×3 contains exactly one instance of the digits from 1 to 9.
Approach For Solving Sudoku Using Recursive Backtracking Algorithm
Like all other Backtracking problems, we can solve Sudoku by one by one assigning numbers to empty cells.
Before assigning a number, we need to confirm that the same number is not present in current row, current column and current 3X3 subgrid.
If number is not present in respective row, column or subgrid, we can assign the number, and recursively check if this assignment leads to a solution or not. If the assignment doesnt lead to a solution, then we try next number for current empty cell. And if none of number (1 to 9) lead to solution, we return false.
