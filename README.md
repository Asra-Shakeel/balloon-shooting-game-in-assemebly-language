# balloon-shooting-game-in-assemebly-language
PROJECT: Balloon Shooting Game
	
Description:
The Balloon Shooting Game is an engaging arcade-style application developed in x86 assembly language, combining technical precision with interactive gameplay. The game challenges players to control a shooter that moves vertically on the screen and shoots arrows to pop descending balloons. This project demonstrates efficient memory usage, real-time graphics rendering, and responsive input handling through direct hardware manipulation. By incorporating assembly-level techniques, the game delivers a seamless and immersive experience.

Objectives:
 	Demonstrate Assembly Language Skills:
Showcase proficiency in low-level programming by implementing a dynamic and functional game.

 	Efficient Hardware Utilization:
Employ assembly commands to interact directly with video memory for smooth rendering and performance optimization.

 	Interactive Gameplay Experience:
Provide players with responsive controls, real-time feedback, and challenging gameplay to enhance user engagement.

 	Dynamic Mechanics and Scoring:
Incorporate features like balloon spawning, player movement, and a real-time scoring system to keep the gameplay challenging and rewarding.

 	Modular and Scalable Codebase:
Ensure the game logic is clean, structured, and maintainable for potential future enhancements.




Features
 	Real-Time User Controls: 
Players use the up and down arrow keys to move the shooter and the spacebar to fire arrows.
The controls are designed for immediate responsiveness.
 	Dynamic Balloon System:
Balloons spawn at random positions and descend toward the shooter.
Missed balloons are tracked, and once the player misses a set number, the game ends.
 	Scoring and Feedback Mechanism:
The game tracks successful hits and missed balloons in real time.
Scores are displayed prominently, and performance is summarized at the end.
 	Interactive Screens:
Game Menu: A detailed introduction screen provides instructions on how to play and allows the user to start the game.
 	Game Over Screen: 
Displays the player's performance and provides an option to restart or exit.
 	Optimized Graphics Rendering:
Direct manipulation of video memory is used to display the shooter, arrows, and balloons.
Smooth updates prevent visual artifacts and enhance gameplay immersion.
 	Well-Defined Game Flow:
The main loop continuously updates the game state, checking for collisions, rendering graphics, and responding to user inputs.
A modular approach separates concerns like player movement, balloon updates, and arrow handling.
 	Clear Visual and Auditory Feedback:
 Collision detection triggers sound effects for successful hits, enhancing player                                              satisfaction.
 Arrows and balloons are visually updated as they move across the screen.





Working:
The Balloon Shooting Game is an arcade-style game implemented in 8086 assembly language, leveraging efficient programming techniques and direct hardware interaction. Below is a detailed explanation of how the game works:
1. Initialization Phase
The program begins by setting up the data segment and initializing required variables such as:
•	Player position.
•	Balloon position.
•	Arrow position and status.
•	Scoring counters (hits and misses).
Video memory is configured to enable direct screen rendering using segment 0B800H.
2. Game Menu:
The game displays a welcome screen with instructions for controlling the player and starting the game.
The program waits for the user to press the Enter key to proceed to the main gameplay loop.
3. Main Gameplay Loop:
The game runs in a continuous loop to update the game state and respond to user input. Key components include:
a. Input Handling
•	The game checks for keyboard input using interrupt 16H.
Player controls:
•	Up arrow key: Moves the player up.
•	Down arrow key: Moves the player down.
•	Spacebar: Fires an arrow.
•	Each keypress updates the respective variables (e.g., direction, arrow status).
b. Game State Updates
Player Movement:
The player's position is updated based on the input direction.
The previous position is cleared, and the new position is rendered on the screen.
Balloon Movement:
The balloon moves downward with each iteration of the loop.
If the balloon reaches the bottom of the screen without being hit, it is counted as a "miss," and a new balloon is spawned.


Arrow Mechanics:
If the arrow is fired, its position is updated as it moves upward.
If the arrow reaches its limit without hitting a balloon, it disappears.
c. Collision Detection
The game checks if the arrow's position matches the balloon's position.
If they collide, the player scores a "hit," and the balloon disappears.
The score is updated, and a new balloon is spawned.
d. Scoring System
The current score (hits and misses) is displayed dynamically on the screen using ASCII characters.
The game ends when the player accumulates a specified number of misses.
4. Game Over:
When the player exceeds the allowable misses, a "Game Over" screen is displayed.
The program resets all game variables and waits for the player to press Enter to restart the game.
5. Visual Rendering:
The game utilizes ASCII art to represent game elements:
The player is represented by an arrow symbol.
Balloons are represented by circular symbols.
The arrow is depicted as a simple line moving upward.
Rendering involves clearing the old position of an object and redrawing it at the updated position.
6. Modular Procedures:
The game is structured using modular procedures for efficient and reusable code:
•	SHOW_SCORE: Updates and displays the score.
•	CLEAR_SCREEN: Clears the screen using interrupt 10H.
•	FIRE_ARROW & FIRE_BALLOON: Handle the logic for spawning new arrows and balloons.
7. Sound Effects:
Simple sound effects are generated using system interrupts when specific events occur, such as:
•	A balloon is hit.
•	The game ends.

Conclusion:
The Balloon Shooting Game is a testament to the power and versatility of x86 assembly language in creating interactive applications. By leveraging direct hardware control and efficient resource management, the game achieves smooth performance and engaging gameplay. Its structured design, real-time mechanics, and dynamic visuals make it both a technical achievement and a source of entertainment. This project not only highlights programming skills but also provides a foundation for exploring further advancements in assembly-based development.

THANK YOU!
