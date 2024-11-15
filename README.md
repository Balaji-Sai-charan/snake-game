Console Snake Game in C++
This project is a classic implementation of the Snake game, built using C++ and designed to run in the console. The game is structured to simulate the movement of a snake that grows in length as it "eats" food and navigates around the screen. The objective is to achieve the highest score by consuming as much food as possible without colliding with the screen edges or the snake's own body.

Game Features
Snake Movement: The snake moves in four directions—up, down, left, and right—controlled by W, A, S, and D keys, respectively.
Dynamic Growth: Each time the snake consumes food, it grows in length, making the game progressively more challenging.
Food Placement: Food appears at random positions on the screen for the snake to consume, and each food item increases the score by 1 point.
Game Over Conditions: The game ends if the snake collides with itself or moves outside the screen boundaries.
Code Structure
The project is divided into several classes and functions for modularity:

1. initializeScreen()
This function initializes the screen size by retrieving the console's width and height. It configures the screen for the snake to move around dynamically based on these dimensions.

2. Coordinate Struct
A simple structure to represent the position (x, y coordinates) of elements like the snake's body segments and food on the screen.

3. SnakeGame Class
The core class for handling the snake's behavior:

Attributes: Stores the snake's length, direction, and body positions.
Functions:
updateDirection: Updates the snake's direction based on player input.
advanceSnake: Moves the snake in the current direction, checks for self-collision, and increases the length if food is consumed.
4. GameBoard Class
This class manages the gameplay and rendering:

Attributes: Maintains the game score, food position, and an instance of SnakeGame.
Functions:
placeFood: Randomly places food on the screen.
render: Clears and re-renders the game board with updated snake and food positions.
updateGame: Advances the snake, checks for collisions, updates the score, and spawns new food if needed.
handleInput: Reads and processes keyboard input for controlling the snake.
5. Main Loop
In the main() function:

Initializes screen settings and creates an instance of GameBoard.
Enters a loop where the game continuously updates, processes input, and renders until a game-over condition is met.
Displays the final score once the game ends.
How to Play
Controls: Use W, A, S, and D keys to move the snake up, left, down, and right, respectively.
Goal: Eat as many food items as possible to increase your score and snake length.
End: The game concludes if the snake collides with itself or moves off-screen.
Requirements
This code uses conio.h and windows.h libraries, which means it is designed to run in a Windows console environment.

Compilation
To compile and run the code, use any C++ compiler that supports Windows libraries. For example:

bash
Copy code
g++ -o SnakeGame SnakeGame.cpp
./SnakeGame
Enjoy the challenge of navigating the snake to the highest score possible!
