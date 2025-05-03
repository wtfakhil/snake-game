# Snake Game

This is a classic Snake game implemented in Python using the Pygame library.

## Dependencies

* **Pygame:** A cross-platform set of Python modules designed for writing video games. You can install it using pip:

    ```bash
    pip install pygame
    ```

## Functionality

The game features the following:

* **Gameplay:** The player controls a snake that moves around the screen, eating food to grow longer. The game ends if the snake collides with the boundaries of the screen or with itself.
* **Controls:** The snake is controlled using the 'a' (left), 'd' (right), 'w' (up), and 's' (down) keys.
* **Score:** The player's score increases as the snake eats more food.
* **Game Over:** When the game ends, a "You Lost!" message is displayed, and the player can choose to play again or quit.

## Code Explanation

The code is structured as follows:

1.  **Initialization:**
    * Imports the `pygame`, `time`, and `random` modules.
    * Initializes Pygame.
    * Defines colors used in the game (white, yellow, black, red, green, blue).
    * Sets the display width and height.
    * Creates the game display (`dis`) and sets the window title.
    * Creates a clock object (`clock`) to control the game's frame rate.
    * Defines the size of the snake block (`snake_block`) and the snake's speed (`snake_speed`).
    * Defines font styles for displaying text (font\_style, score\_font).

2.  **Functions:**
    * `Your_score(score)`: Renders and displays the player's score on the screen.
    * `our_snake(snake_block, snake_list)`: Draws the snake on the screen as a series of rectangles.
    * `message(msg, color)`: Renders and displays a message on the screen (e.g., "You Lost!").
    * `gameLoop()`: Contains the main game logic.

3.  **`gameLoop()` Function Details:**
    * Initializes game variables (`game_over`, `game_close`, snake position, snake list, snake length, food position).
    * The main game loop (`while not game_over`):
        * The game over loop (`while game_close == True`): Displays the "You Lost!" message and handles player input to play again (C) or quit (Q).
        * Event handling (`for event in pygame.event.get()`): Handles events such as key presses (for snake movement) and quitting the game.
        * Snake movement: Updates the snake's position based on the player's input.
        * Boundary collision detection: Checks if the snake has hit the screen boundaries.
        * Drawing: Fills the screen with blue, draws the food, and draws the snake.
        * Snake self-collision detection: Checks if the snake has collided with itself.
        * Score update: Displays the current score.
        * Display update: Updates the entire display to show the changes.
        * Food consumption: Checks if the snake has eaten the food, and if so, generates new food and increases the snake's length.
        * Game speed: Controls the game's speed using `clock.tick()`.
    * Quits Pygame and the program after the game loop ends.

## How to Run

1.  **Install Dependencies:**
    * Install Pygame using pip: `pip install pygame`
2.  **Save the Code:**
    * Save the code as a `.py` file (e.g., `snake_game.py`).  Note: You only need one copy of the code.  You don't need `main.py`, `pygame.py`, and `snake.py` with the same content.
3.  **Execute the Script:**
    * Run the script from the command line: `python snake_game.py`

The Snake game window will appear, and you can start playing.
