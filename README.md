# README

- Read me for the python project "Asteroids", by: Dipankar Mohanty.

# ABOUT

Asteriods is python based game, using the third party library pygame, and guided with help of platform Bootdev (link: https://www.boot.dev). This project was created and developed to understand the concepts of OOPS and with my own eagerness to learn and practise git add, commits, status, and log, alongside version schematics.

# GIST

- The project uses third party library pygame, to simulate a game engine running in the background, using various inputs from the system, to call upon draw, update and kill objects(or sprites) methods of the sprite objects, and visually printing on the floating windows. 
- The triangle is the main player, using AWSD to control the movements, and spacebar to shoot, which destroys small and splits bigger asteroids. The hazard are the asteroid and upon touch to player (collision) declares a GAME OVER.
- Survive long enough and hope we all survive the wrath of the asteroids.

#  DESCRIPTION

* Warning: Class with (*) symbol on their name indicate, they were provided by the instructor to ease the burden and focus on the concepts to understand.

- (*)circleshape - The base class, parent to all the objects(asteroid, bullet, player). It inherits from pygame's sprite to handle basic positional, and 2D vector operations. It includes the automatic group managment for faster calculation, 2D physical vector attributes to handle positional & velocity, update & draw methods for the children to render themselves onto the screen based on the user input, and finally collision method acting as an hit box.
- (*)asteroidfield -  It is a state manager working in the backend of the game, to continously spawn the asteroids from the edges onto the screen, creating the various instances of the asteroid class.
- Asteroid - Obstacles, child class of circleshape, and generated at random by asteroidfield, inherits all properties of circleshape and overrides the update with constant positional update based on delta time, draw with pygame.draw.circle to draw on the screen, and comes with additional method split to divide itself into two or kill itself upon collision with bullet.
- Player - A child class of circleshape, inheriting all its properties acting as the skeleton, causing player movement and hitbox, where update is replaced with pygame to check for constant input, basing its call move|rotate|shoot on key inputs of the user, draw with generic triangles creation, and additional move(updates the player position vector using vector calculation), rotate(pygame rotate method to rotate the positional vector of the player based on dt) and shoot(creates a bullet object, at the position of the player, assigning with itself a velocity vector based on the player vector)
- Shot - A child class of circleshape, inheriting all its properties, created upon call of player shot().method at player's position, using update to update it's position using velocity vector and draw to render itself on the screen.
- CONSTANTS - Not a class but handles the important constants to keep consistency across the file and ease of updating the weights should it require to change the values, reflected across the whole program in one edit.

# THANKS

- I want to thanks the boot.dev for such on hands on project, especially author of the project, Sarah Schulte
(Creator of BASH stack, the tool for web apps in bash, awk, sed, and htmx).

[![Boot.dev Build Asteroids using Python and Pygame certificate](https://qvault-webapp-dynamic-assets.storage.googleapis.com/certificates/d708c5bc-43ac-4576-a997-5a8009284842.jpeg?v=1788185952)](https://www.boot.dev/certificates/d708c5bc-43ac-4576-a997-5a8009284842)
