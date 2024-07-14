# Sudoku Solver

## Overview

This project implements a Sudoku solver in C++. The solver reads a Sudoku puzzle either from user input or from a file, validates the input, and then employs a backtracking algorithm to solve the puzzle.

## Features

- **Input Methods**: Choose between manual entry or reading from a file.
- **Validation**: Ensures that input values are within valid ranges (0-9).
- **Backtracking Algorithm**: Utilizes a recursive approach to solve the puzzle efficiently.

## Technical Details

### Class Structure

1. **`SudokuGrid`**:
   - Manages the 9x9 grid and handles user input.
   - Contains methods for displaying the grid, setting, and getting cell values.

2. **`SudokuSolver`**:
   - Contains the logic for solving the Sudoku puzzle using backtracking.
   - Tracks recursive calls to provide statistics on the solving process.

### Input Format

- For manual input, the user is prompted to enter values for each cell (0 for empty cells).
- For file input, the file should contain 81 integers separated by spaces, representing the Sudoku grid.

### Example Input File

```
5 3 0 0 7 0 0 0 0
6 0 0 1 9 5 0 0 0
0 9 8 0 0 0 0 6 0
8 0 0 0 6 0 0 0 3
4 0 0 8 0 3 0 0 1
7 0 0 0 2 0 0 0 6
0 6 0 0 0 0 2 8 0
0 0 0 4 1 9 0 0 5
0 0 0 0 8 0 0 7 9
```

### Example Usage

1. Compile the program using a C++ compiler:
   ```bash
   g++ -o sudoku_solver sudoku_solver.cpp
   ```

2. Run the program:
   ```bash
   ./sudoku_solver
   ```

3. Follow the prompts to input the Sudoku puzzle.

### Example Output

```
++=====================================++
|| 5  3  |   7  |          ||
++-----------++-----------++-----------++
|| 6     | 1  9  5 |        ||
++-----------++-----------++-----------++
||    9  8 |       |  6     ||
++-----------++-----------++-----------++
|| 8     |   6     |    3   ||
++-----------++-----------++-----------++
|| 4     | 8  3   |      1  ||
++-----------++-----------++-----------++
|| 7     | 2     |   6     ||
++-----------++-----------++-----------++
||    6  |       | 2  8     ||
++-----------++-----------++-----------++
||        | 4  1  9 |       ||
++-----------++-----------++-----------++
||        |       | 8  7  9 ||
++=====================================++

Calculating...
Puzzle solved!

Recursive calls: 12
```

## Complexity Analysis

The time complexity of the backtracking algorithm used in this solver is generally \(O(9^{n})\), where \(n\) is the number of empty cells in the Sudoku puzzle. In the worst case, this can lead to a significant number of recursive calls, but in practice, most puzzles can be solved much more quickly.
