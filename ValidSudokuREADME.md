# leet-day61

# Sudoku Validator

This C++ program checks whether a given 9x9 Sudoku board is valid according to the Sudoku rules:

1. Each row must contain the digits 1-9 without repetition.
2. Each column must contain the digits 1-9 without repetition.
3. Each of the nine 3x3 sub-boxes of the grid must contain the digits 1-9 without repetition.

## How to Use

1. Open a C++ development environment or text editor.
2. Create a new C++ source file (e.g., `sudoku_validator.cpp`).
3. Copy and paste the provided C++ code into the source file.
4. Save the file.

### Compilation

To compile the program, open your terminal or command prompt, navigate to the folder containing the source file, and run the following command:

```bash
g++ sudoku_validator.cpp -o sudoku_validator
```

### Execution

After successful compilation, you can run the program by executing the following command:

```bash
./sudoku_validator
```

The program will prompt you to input the Sudoku board as a 9x9 grid. You should provide the board as nine lines of input, each containing nine characters. Use digits from 1 to 9 to represent the numbers in the Sudoku puzzle and use a period (`.`) for empty cells. Here's an example input:

```plaintext
53..7....
6..195...
.98....6.
8...6...3
4..8.3..1
7...2...6
.6....28.
...419..5
....8..79
```

After entering the board, press Enter, and the program will check if the Sudoku board is valid. It will display "Valid" if the Sudoku board follows the rules and "Invalid" otherwise.

### Example

Here's how the program works with the provided example input:

```plaintext
53..7....
6..195...
.98....6.
8...6...3
4..8.3..1
7...2...6
.6....28.
...419..5
....8..79

Valid
```

## Implementation Details

The program utilizes a straightforward approach to validate the Sudoku board:

1. It uses three sets of unordered sets: one for rows, one for columns, and one for sub-grids.
2. It iterates through each cell in the 9x9 grid, checking for duplications in rows, columns, and sub-grids.
3. If a duplication is found, the board is marked as "Invalid."

## Constraints

- The input board must be a 9x9 grid.
- The program assumes that the input adheres to Sudoku rules (i.e., contains only digits 1-9 and '.' for empty cells).

