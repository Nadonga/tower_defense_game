Tower Defense Game (OOP Edition)
A 2D tower defense game built in Python using Pygame 🎮. The project uses modular design and object oriented programming to manage enemies, towers, maps, and game flow.

Note
This project is based on an existing open source implementation used for learning and academic submission.

Attribution & Credit
Original creator: techwithtim
Original repository: Tower-Defense-Game

Project Structure and File Breakdown

main.py 🚀
Starts the game and controls the main execution loop.

Abstraction
Hides full game setup inside a single entry point. Only start logic appears here.

Encapsulation
Stores game objects like map, towers, and enemies inside controlled runtime flow instead of global access.

Inheritance
Connects all object systems like enemies and towers under one game structure.

Polymorphism
Calls update() and draw() across different game objects without checking types.

game.py 🎯
Handles core gameplay logic, state updates, and rendering.

Abstraction
Separates game rules and update cycles from UI and setup.

Encapsulation
Keeps score, lives, waves, and active objects inside one game class.

Inheritance
Acts as the central controller used by other modules.

Polymorphism
Uses shared methods like update() and draw() across towers, enemies, and projectiles with different behavior.

enemies folder 👾
Defines enemy types, movement, and health system.

Abstraction
Base enemy class defines path movement and shared logic.

Encapsulation
Stores health, speed, and position inside each enemy object.

Inheritance
Specific enemy types inherit from base enemy class and reuse movement logic.

Polymorphism
Different enemies override update() and draw() with unique stats and visuals.

towers folder 🏰
Handles tower placement, attack system, and targeting.

Abstraction
Base tower class defines range, cooldown, and attack behavior.

Encapsulation
Tower stats like damage and range are kept inside the class and modified through methods.

Inheritance
Multiple tower types inherit shared attack and targeting logic.

Polymorphism
Each tower overrides attack behavior while keeping the same method interface.

maps folder 🗺️
Stores level layouts and path data.

Abstraction
Map class defines grid layout and enemy path.

Encapsulation
Grid data and path coordinates are stored inside map objects.

Inheritance
Map variations reuse base map structure.

Polymorphism
Different maps use the same interface but return different paths and layouts.

menu folder 📋
Handles start screen and navigation.

Abstraction
Menu system manages buttons and screen transitions.

Encapsulation
Button states and input logic are stored inside menu class.

Inheritance
UI components like buttons can share a base structure.

Polymorphism
Different buttons use the same click() method but trigger different actions.

run.py ▶️
Entry point for launching the game.

Abstraction
Runs the full game without exposing internal logic.

Encapsulation
Keeps execution separate from game modules.

Inheritance
No inheritance used. Acts as connector.

Polymorphism
Triggers unified start methods from different modules.

requirements.txt 📦
Lists required Python packages.

Purpose
Ensures Pygame installs correctly for running the project.

.gitpod.yml ☁️
Configures cloud development environment.

Purpose
Sets up workspace automatically for consistent development.

Dockerfile 🐳
Defines container setup for the project.

Purpose
Ensures same environment across systems.

Built With
Python 3.x 🐍
Pygame 🎮
