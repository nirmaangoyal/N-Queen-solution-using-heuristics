# N-Queen Solver

This project implements a heuristic solution to the N-Queen problem using JavaScript. The N-Queen problem is the challenge of placing N chess queens on an N×N chessboard so that no two queens threaten each other.

## Technical Overview

The solution uses a randomized initial placement followed by iterative improvement to solve the N-Queen problem. Here's a detailed explanation of how the code works:

### 1. Board Initialization

- The chessboard is represented as a 2D array (`arrBoard`) where 1 indicates the presence of a queen and 0 indicates an empty cell.
- The `placeInitialQueens(arrBoard)` function is used to place queens randomly on the board, one in each row.

### 2. Finding the Most Threatened Queen

The `findMostThreatenedQueen(arrBoard)` function identifies the queen under the highest threat:

- It iterates through all queens on the board.
- For each queen, it calculates the number of threats using `findNumberOfThreats(arrBoard, row, col)`.
- It keeps track of the queen with the maximum number of threats.
- If no threats are found (i.e., a solution is reached), it returns -1.

### 3. Calculating Threats

The `findNumberOfThreats(arrBoard, row, col)` function calculates how many queens are threatening a specific position:

- It checks for threats in the same column.
- It checks for diagonal threats in all four directions: up-left, up-right, down-left, and down-right.
- The function returns the total number of threats.

### 4. Finding the Least Threatened Column

The `findLeastThreatenedColumn(arrBoard, q)` function finds the safest column to move the most threatened queen:

- It temporarily removes the queen from its current position.
- It then checks every other column in the same row.
- For each position, it calculates the number of threats.
- It keeps track of the position with the minimum number of threats.
- Finally, it moves the queen to the least threatened column.

### 5. Main Algorithm Flow

The main algorithm (not explicitly shown in the provided code) would typically work as follows:

1. Initialize the board with random queen placements.
2. Find the most threatened queen.
3. If no queen is under threat, the problem is solved.
4. Otherwise, move the most threatened queen to its least threatened column.
5. Repeat steps 2-4 until a solution is found or a maximum number of iterations is reached.

## HTML Interface

The project includes a simple HTML interface that allows users to:

- Input the number of queens (N).
- Generate a chessboard of the specified size.
- Visualize the solution process (implementation details not provided in the given code).



## Future Improvements

- Implement a visualization of the solving process in the HTML interface.
- Add a maximum iteration limit to prevent infinite loops for unsolvable configurations.
- Optimize the algorithm for larger board sizes.

## How to Use

1. Open the HTML file in a web browser.
2. Enter the desired number of queens.
3. Click "Generate Chessboard" to start the solving process.
4. The solution (or best attempt) will be displayed on the chessboard.

Feel free to contribute to this project by optimizing the algorithm or improving the user interface!