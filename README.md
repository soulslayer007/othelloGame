## Othello Board Game

This project implements the classic board game Othello (also known as Reversi) using JavaScript. The game includes functionalities for initializing the game board, handling player moves, finding valid moves, flipping opponent's pieces, and determining the game's end result.

## Introduction

Othello is a two-player strategy board game played on an 8x8 grid. The game starts with four discs placed in the center of the board, with two black discs and two white discs. Players take turns placing discs on the board, with the goal of surrounding and capturing the opponent's discs. The game ends when neither player can make a valid move, and the player with the most discs on the board wins.

This project implements the game logic using JavaScript classes for the board, cells, and game management. It also provides a simple user interface for playing the game in a web browser.

## Features

- **Dynamic Board:** The game board is dynamically generated based on the specified width.
- **Interactive Interface:** Players can click on cells to place their discs and make moves.
- **Valid Move Detection:** The game highlights valid moves for the current player.
- **Turn-Based Gameplay:** Players take turns placing discs on the board.
- **End Game Detection:** The game detects when no valid moves are available for either player and ends the game.
- **Result Display:** After the game ends, the result (winner and score) is displayed.

## Usage

To play the game, simply open the `index.html` file in a web browser. The game board will be displayed, and players can take turns clicking on cells to place their discs. Valid moves are highlighted, and the game automatically detects when the game ends.

## File Structure

- **`index.html`:** The HTML file containing the game interface.
- **`scripts/`:** This directory contains JavaScript files for the game logic.
  - **`cell.js`:** Defines the `Cell` class representing individual cells on the game board.
  - **`board.js`:** Defines the `Board` class representing the game board and managing game state.
  - **`index.js`:** Initializes the game and handles user interaction.

## Functions Used
Sure, let's break down the functions used in the provided JavaScript code:

1. **Board Class:**
    - `constructor(width)`: Initializes a new instance of the `Board` class with the specified width (default is 8).
    - `initBoard()`: Initializes the board by creating cells for each position and setting up initial game state.
    - `putInitialNuts()`: Places initial game pieces (nuts) on the board.
    - `getNuts(owner)`: Returns an array of nuts owned by the specified player or all nuts if no owner is specified.
    - `changeTurn()`: Changes the turn from one player to another.
    - `setOwner(x, y, owner)`: Sets the owner of the cell at the specified coordinates.
    - `findMoves()`: Finds all possible moves for the current player.
    - `getEmptyNeighborsOfCell(x, y)`: Returns an array of empty neighboring cells for the specified cell.
    - `crossAllDirectionsToCell(cx, cy, centerNut)`: Finds valid moves in all directions from a given cell.
    - `isValidMove(x, y)`: Checks if a move to the specified coordinates is valid.
    - `placeNutTo(x, y)`: Places a nut on the board at the specified coordinates and updates the game state.
    - `gameResult()`: Calculates and returns the result of the game, including the winner and number of nuts owned by each player.

2. **Cell Class:**
    - `constructor(x, y, owner)`: Initializes a new instance of the `Cell` class with the specified coordinates and owner.
    - `pos()`: Returns the coordinates of the cell as an array `[x, y]`.
    - `owner`: Getter and setter for the owner property of the cell.
    - `neighbors()`: Returns an array of coordinates representing neighboring cells.

3. **OthelloGame Class:**
    - `constructor(options)`: Initializes a new instance of the `OthelloGame` class with the specified options.
    - `initGame()`: Initializes the game by creating the game board and rendering it in the specified HTML element.
    - `reRender()`: Updates the game board by re-rendering it in the HTML element.
    - `createNutElm(type, validMove, turn)`: Creates a DOM element representing a game piece (nut) with the specified type, validMove status, and turn.
    - `createRowElm(y)`: Creates a DOM element representing a row of cells on the game board.
    - `handleCellClick(x, y)`: Event handler for cell click events, which places a nut on the board at the specified coordinates.
    - `createCellElm(x, y)`: Creates a DOM element representing a single cell on the game board.

These functions and classes work together to implement the logic and user interface for playing the Othello game.

### Features:

1. **Game Initialization**: The `Board` class initializes the game board with a specified width and places initial pieces on the board.

2. **Valid Moves Calculation**: The game calculates valid moves for the current player based on the game rules.

3. **Player Interaction**: Players can click on empty cells to place their pieces. The game validates the move and flips opponent's pieces accordingly.

4. **Game End Detection**: The game detects when no more valid moves are available for both players, indicating the end of the game. It then calculates and displays the winner.

### Usage:

1. Clone the repository: `git clone <repository-url>`
2. Open `index.html` in a web browser.
3. Click on empty cells to make a move.
4. Continue playing until the game ends.

### Future Improvements:

1. **AI Opponent**: Implement an AI opponent for single-player mode.
2. **Customization Options**: Allow users to customize game settings such as board size and piece colors.
3. **Game History**: Implement functionality to review past moves and game history.

Feel free to contribute to this project and improve its features!
