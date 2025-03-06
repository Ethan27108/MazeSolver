# Maze Solver

This project is a maze-solving simulation using Pygame. It creates a maze and simulates 32 "people" attempting to navigate through it. The simulation evolves the "people" based on their performance until the maze is solved.

## Requirements

- Python 3.x
- Pygame

## Installation

1. Install Python 3.x from [python.org](https://www.python.org/).
2. Install Pygame using pip:
   ```sh
   pip install pygame

## Usage

Run the `Maze.py` script to start the simulation.

## How It Works

### Maze Generation

The maze is generated using the `baseMaze` function, which creates a 2D list representing the maze structure. The maze consists of walls (`"_"` and `"|"`) and open spaces (`" "`). The goal is represented by `"Ω"`.

### Simulation

The main loop of the simulation is in the `while gameOn` block. It performs the following steps:

1. Increments the `generaltrack` and `amount` variables.
2. Creates 32 "people" who attempt to navigate the maze.
3. Each "person" is given random moves using the `addingMoves` function.
4. The `moving` function simulates the movement of each "person" through the maze and updates their score based on their performance.
5. The best-performing "person" is identified, and their moves are used to evolve the other "people".
6. The simulation continues until the maze is solved or the game is over.

## Functions

- **`baseMaze(maze)`**: Generates the initial maze structure.
- **`baseMazePrint(printmaze)`**: Prints the initial maze using Pygame.
- **`printMaze(printmaze)`**: Prints the updated maze using Pygame.
- **`addingMoves(lst)`**: Adds random moves to the list of moves for a "person".
- **`rowAdder(row, col, underScoreadd, addmaze)`**: Updates the maze based on the current position.
- **`moving(guy, rowcol, underScoreChange, amount, playmaze)`**: Simulates the movement of a "person" through the maze and updates their score.

## Pygame Initialization

The Pygame library is used to visualize the maze and the movement of the "people". The screen is set to 800x800 pixels, and the maze is displayed using rectangles.

## Example Output

The simulation prints the time taken to solve the maze once the game is over.

## License

This project is licensed under the MIT License.
