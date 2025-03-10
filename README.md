# N-Queen-problems_202401100400194Here's a template for a **README file** for a project focused on the **N-Queen problem**. This file provides an explanation of the problem, the approach to solving it, and instructions for running the code.

---

# N-Queen Problem Solver

## Description

The **N-Queen problem** is a classic combinatorial problem in computer science and artificial intelligence. The goal is to place **N queens** on an **N×N chessboard** in such a way that no two queens threaten each other. A queen can attack another queen if they are placed on the same row, column, or diagonal. The problem asks to find a solution where all queens are placed in a way that no two queens can attack each other.

### Problem Statement
Given an integer `N`, the task is to find all possible solutions to place N queens on an N×N chessboard such that:
- No two queens are on the same row.
- No two queens are on the same column.
- No two queens are on the same diagonal.

### Example
For `N = 4`, the solution is:
```
- Q - -
- - - Q
Q - - -
- - Q -
```

There are two distinct solutions for the 4x4 board.

---

## Approach

This project uses **backtracking** to solve the N-Queen problem. The backtracking algorithm explores all possible placements of queens on the board, and when it encounters an invalid configuration, it backtracks to the previous step and tries a different approach.

The backtracking algorithm follows these steps:
1. Start placing queens row by row.
2. For each row, try placing a queen in each column.
3. After placing a queen, check if it is safe from attacks by any previously placed queens (i.e., check if no two queens are in the same column or diagonal).
4. If placing the queen leads to a valid solution, move to the next row.
5. If all queens are placed successfully, record the solution.
6. If at any point no valid position is found in a row, backtrack to the previous row and try a different placement.

### Key Points:
- **Safe Check**: At each step, we check whether placing a queen at a given position will lead to an attack. This involves checking the column and diagonals.
- **Backtracking**: If a solution is not found in a particular configuration, the algorithm backtracks and tries a new configuration.

---

## Installation

To use this solution, clone this repository to your local machine:

```bash
git clone https://github.com/your-username/n-queen-solver.git
cd n-queen-solver
```

### Dependencies

- Python 3.x
- No external libraries are required, but using an IDE like VS Code or PyCharm is recommended for easier debugging.

---

## How to Run

1. **Clone the repository** (if not done already):

    ```bash
    git clone https://github.com/your-username/n-queen-solver.git
    cd n-queen-solver
    ```

2. **Run the script**:

    In your terminal, run the Python script:

    ```bash
    python nqueen_solver.py
    ```

    You will be prompted to enter a value for `N` (the size of the chessboard). The program will output all possible solutions for the N-Queen problem.

3. **Input and Output**:

    - Input: The program will ask for an integer input `N` (size of the board).
    - Output: The program will print all solutions, each solution displayed as a grid where queens are represented by `Q`.

---

## Example Run

```bash
Enter the size of the board (N): 4
Solution 1:
- Q - -
- - - Q
Q - - -
- - Q -

Solution 2:
- - Q -
Q - - -
- - - Q
- Q - -
```

---

## Project Structure

```
n-queen-solver/
├── nqueen_solver.py       # Python script containing the N-Queen solver
├── README.md              # This README file
└── solution_output.txt    # Optional file to save solutions
```

---

## Algorithms and Techniques Used

- **Backtracking**: The algorithm is based on the backtracking approach to explore all possible placements of queens on the board.
- **Optimization**: Each time a queen is placed, we check if the current board configuration is valid (i.e., no queens are threatening each other).

---

## Contributing

Feel free to fork this project, open issues, and submit pull requests. Contributions are always welcome! If you improve the algorithm or add new features, please document your changes.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

- The N-Queen problem is a classical problem often used to demonstrate backtracking algorithms.
- Thanks to the contributors of various open-source repositories on backtracking algorithms.

---

Let me know if you need any modifications or if you'd like to expand on any sections!
