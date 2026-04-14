# Breakout Game
A Python-based arcade application that recreates the classic "Breakout" game using Object-Oriented Programming (OOP) concepts and the Pygame library.
This game simulates a physics-based environment where the player controls a paddle to bounce a ball into a grid of blocks, aiming to destroy them all without letting the ball fall off the bottom of the screen.
<br>

## How the Code Works & Pygame Usage
The code relies heavily on Pygame, a popular set of Python modules designed for writing video games. Pygame provides the core infrastructure for rendering graphics, handling the main game loop, and capturing user input. The following explains how the game works :

- **Initialization & Display:** The script uses pygame.init() to start the engine and pygame.display.set_mode() to create an 800x600 window.

- **Sprites & Groups:** The core mechanism of the game revolves around Pygame's pygame.sprite.Sprite class. The Block, Ball, and Player objects all inherit from this base class. This allows the game to efficiently manage them using pygame.sprite.Group(), making it easy to render all objects at once (allsprites.draw()) and handle interactions.

- **Collision Detection:** The code uses Pygame's built-in collision functions, specifically pygame.sprite.spritecollide(), to detect when the ball hits the paddle or the blocks.

- **Math & Physics:** The math module is utilized to calculate the ball's trajectory. By converting the ball's direction into radians, math.sin and math.cos determine the X and Y coordinate updates frame-by-frame. The paddle also features a dynamic bounce calculation, altering the ball's trajectory depending on where it strikes the paddle.

- **Game Loop:** A while not exit_program: loop keeps the game running, locked to 30 frames per second using pygame.time.Clock(). Inside this loop, the screen is wiped clean, events (like quitting) are processed, object positions are updated, and everything is redrawn to the screen.
 

## Features
- Player-controlled paddle tracking the user's mouse position.

- Dynamic ball physics that calculate bounce angles based on paddle impact location.

- Automated grid generation for the target blocks.

- Real-time collision detection and block destruction.

- Win/Loss state handling (Game Over text).

- Demonstrates OOP concepts which are Inheritance, Encapsulation, and Polymorphism via Pygame's Sprite system.
<br>

## Project Structure
- **Block class:** Represents the static, breakable targets at the top of the screen.

- **Ball class:** Manages the speed, trajectory, boundary bouncing, and trigonometric movement updates.

- **Player class:** Represents the user's paddle and updates its X-coordinate based on mouse movement.

- **Main Game Loop:** Coordinates framerate, processes event handling (quitting), updates object states, checks for collisions, and renders the graphics to the screen.
 

## Output
<img width="1130" height="884" alt="image" src="https://github.com/user-attachments/assets/7c500b15-ce6e-452d-85d9-df050a540264" />
<br><br> <!-- This statement is used for giving space -->

<img width="1054" height="837" alt="image" src="https://github.com/user-attachments/assets/26da778b-efa7-4f36-b6b8-85a142a8e54e" />
<br><br> <!-- This statement is used for giving space -->

<img width="1053" height="817" alt="image" src="https://github.com/user-attachments/assets/9a6ae40e-b2f7-41bb-89c1-27b3d5c06ada" />
<br><br> <!-- This statement is used for giving space -->

<img width="1131" height="879" alt="image" src="https://github.com/user-attachments/assets/9b28d643-fb16-4428-a6ec-3265c93a41e4" />
<br><br> <!-- This statement is used for giving space -->

<img width="1043" height="817" alt="image" src="https://github.com/user-attachments/assets/9c02ef73-824e-4066-85af-b817a2853d81" />
<br><br> <!-- This statement is used for giving space -->

<img width="1021" height="800" alt="image" src="https://github.com/user-attachments/assets/528b9ec0-a3df-49e7-9696-2da4312edcb1" />
<br><br> <!-- This statement is used for giving space -->




