
# Sudoku Solver — x86 Assembly (MASM)

A console-based Sudoku solver written in x86 Assembly using the MASM assembler and Irvine32 library. The program accepts a 9x9 Sudoku grid as input and solves it using a backtracking algorithm.


## How It Works

The solver uses recursive backtracking. It scans the grid for empty cells, tries placing digits 1–9, validates each placement against row, column, and 3x3 box constraints, and backtracks if no valid digit fits.


## Key Procedures

- `SolveSudoku` — Recursive backtracking engine
- `findEmptyPlace` — Locates the next unfilled cell
- `isValidPlace` — Validates a digit against all constraints
- `isPresentInRow` — Checks if a digit exists in a given row
- `isPresentInCol` — Checks if a digit exists in a given column
- `isPresentInBox` — Checks if a digit exists in the 3x3 subgrid
- `inputgrid` — Handles user input row by row with validation
- `PrintGrid` — Renders the grid with borders to the console
- `Authentication0` / `Authentication1` — Validates input ranges (0–9 and 1–9)


## Requirements

- Windows OS
- MASM (Microsoft Macro Assembler)
- [Irvine32 Library](http://asmirvine.com/)


## Building and Running

1. Link the Irvine32 library to your project.
2. Assemble and link using MASM:
```
ml /c /coff sudoku.asm
link /subsystem:console sudoku.obj irvine32.lib kernel32.lib user32.lib
```
3. Run the resulting `.exe`.



## Input Format

Enter the grid row by row when prompted. Use `0` for empty cells. Only values 0–9 are accepted. Invalid inputs are rejected and re-prompted.


## Output

If a solution exists, the solved grid is printed to the console with row and column separators. If no solution exists, an appropriate message is displayed.


## Authors

HAM Team
