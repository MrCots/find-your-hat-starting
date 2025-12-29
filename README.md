# Find Your Hat

A terminal-based maze game written in JavaScript running on Node.js.

## Project Steps

### 1. Field Class Setup
- Created a `Field` class to represent the game board.
- The constructor accepts a 2D array representing the grid (holes, hat, background).
- Initialized player position at `(0,0)`.

### 2. Visualizing the Board
- Implemented a `print()` method in the `Field` class.
- Uses `.join()` to convert the 2D array into a string for console output.

### 3. Game Loop and User Input
- Added `runGame()` to handle the main game loop until the game is won or lost.
- Integrated `prompt-sync` to accept user input.
- Added `askQuestion()` to handle asking for input and updating the current location.
- Stored `locationX` and `locationY` on the class instance to track player position.

### 4. Win/Loss Logic
- Created helper methods to test the current location:
    - `isInBounds()`: Checks if the player is within the field.
    - `isHat()`: Checks if the player found the hat.
    - `isHole()`: Checks if the player fell in a hole.

### 5. Field Generation
- Added a static method `generateField(height, width, percentage)` to the `Field` class.
- Generates a randomized 2D array with a hat and holes.
- Ensures the hat is not placed at the starting position `(0,0)`.

## How to Play

1. Open your terminal.
2. Run the game with `node main.js`.
3. Enter `U`, `D`, `L`, or `R` to move the player (`*`). => Changed for traditional game WASD. as per codeacademy suggestions: "Change the input mapping to a more typical gaming setup. The WASD keys are often used on QWERTY keyboards to represent up, left, down, and right, respectively."
4. Avoid holes (`O`) and try to reach the hat (`^`).