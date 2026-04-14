# Breakout Game
A Python-based arcade application that recreates the classic "Breakout" game using Object-Oriented Programming (OOP) concepts and the Pygame library.
This game simulates a physics-based environment where the player controls a paddle to bounce a ball into a grid of blocks, aiming to destroy them all without letting the ball fall off the bottom of the screen.

## How the Code Works & Pygame Usage
The code relies heavily on Pygame, a popular set of Python modules designed for writing video games. Pygame provides the core infrastructure for rendering graphics, handling the main game loop, and capturing user input. The following explains how the game works :

- **Initialization & Display:** The script uses pygame.init() to start the engine and pygame.display.set_mode() to create an 800x600 window.

Sprites & Groups: The core mechanism of the game revolves around Pygame's pygame.sprite.Sprite class. The Block, Ball, and Player objects all inherit from this base class. This allows the game to efficiently manage them using pygame.sprite.Group(), making it easy to render all objects at once (allsprites.draw()) and handle interactions.

Collision Detection: The code uses Pygame's built-in collision functions, specifically pygame.sprite.spritecollide(), to detect when the ball hits the paddle or the blocks.

Math & Physics: The math module is utilized to calculate the ball's trajectory. By converting the ball's direction into radians, math.sin and math.cos determine the X and Y coordinate updates frame-by-frame. The paddle also features a dynamic bounce calculation, altering the ball's trajectory depending on where it strikes the paddle.

Game Loop: A while not exit_program: loop keeps the game running, locked to 30 frames per second using pygame.time.Clock(). Inside this loop, the screen is wiped clean, events (like quitting) are processed, object positions are updated, and everything is redrawn to the screen.

