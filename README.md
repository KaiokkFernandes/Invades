# Space Invaders++: Advanced C++ Game Using Allegro Library

## Table of Contents

- [Introduction](#introduction)
- [Game Overview](#game-overview)
- [Project Structure](#project-structure)
- [Key Components](#key-components)
  - [Graphics and Rendering](#graphics-and-rendering)
  - [Game Mechanics](#game-mechanics)
  - [AI Pathfinding (Dijkstra's Algorithm)](#ai-pathfinding-dijkstras-algorithm)
  - [Data Structures (Balanced Binary Trees)](#data-structures-balanced-binary-trees)
- [Installation and Setup](#installation-and-setup)
- [Usage Instructions](#usage-instructions)
- [Contributing Guidelines](#contributing-guidelines)
- [License](#license)
- [Acknowledgements](#acknowledgements)

---

## Introduction

Welcome to **Space Invaders++**, a modern take on the classic arcade game **Space Invaders**, developed in C++ using the **Allegro** game development library. This project incorporates advanced programming concepts such as **Dijkstra's Algorithm** for enemy pathfinding and **balanced binary trees** for efficient data management, providing a rich learning experience for developers interested in game development and advanced algorithms.

---

## Game Overview

**Space Invaders++** is a 2D shooter game where the player controls a spaceship at the bottom of the screen, aiming to eliminate waves of alien invaders descending from the top. The game introduces intelligent enemy behaviors, dynamic difficulty adjustment, and efficient data handling through advanced algorithms and data structures.

---

## Project Structure

The project's source code is organized into the following directories and files:

- **src/**: Contains all source code files.
  - `main.cpp`: The entry point of the game.
  - `Game.hpp` / `Game.cpp`: Core game loop and state management.
  - `Player.hpp` / `Player.cpp`: Player character implementation.
  - `Enemy.hpp` / `Enemy.cpp`: Enemy character implementation with AI.
  - `Graphics.hpp` / `Graphics.cpp`: Rendering and animation handling.
  - `Pathfinding.hpp` / `Pathfinding.cpp`: Implementation of Dijkstra's Algorithm.
  - `DataStructures.hpp` / `DataStructures.cpp`: Implementation of balanced binary trees.
- **assets/**: Contains game assets like images and sounds.
- **docs/**: Contains documentation files.
- **README.md**: Provides an overview and instructions.
- **Makefile**: Build automation script.

---

## Key Components

### Graphics and Rendering

**Allegro Library** is used for all graphics and rendering tasks:

- **Initialization**: Sets up the display, keyboard, and timer.
- **Sprites and Animations**: Manages loading and displaying sprite sheets.
- **Double Buffering**: Implements double buffering to prevent screen flickering.
- **Event Handling**: Captures and processes user inputs and game events.

### Game Mechanics

The game mechanics involve:

- **Player Movement**: The player can move left or right and shoot bullets.
- **Enemy Waves**: Enemies descend in waves with increasing difficulty.
- **Collision Detection**: Detects collisions between bullets and enemies using bounding box algorithms.
- **Score and Lives**: Tracks player score and remaining lives.

### AI Pathfinding (Dijkstra's Algorithm)

Enemies use **Dijkstra's Algorithm** for intelligent pathfinding:

- **Grid Representation**: The game area is divided into a grid for pathfinding.
- **Weighted Graph**: Each grid cell represents a node in a graph with weights based on difficulty.
- **Shortest Path Calculation**: Enemies calculate the shortest path to the player, allowing for dynamic movement patterns.
- **Dynamic Obstacles**: The algorithm accounts for moving obstacles, recalculating paths as necessary.

### Data Structures (Balanced Binary Trees)

The game uses **Balanced Binary Trees** for efficient data management:

- **High Scores**: Stores and retrieves high scores efficiently.
- **Entity Management**: Manages active game entities (enemies, bullets) for quick insertion and deletion.
- **Balanced Insertion**: Ensures the tree remains balanced after operations to maintain O(log n) performance.
- **Traversal**: In-order traversal is used to process entities in a sorted manner when needed.

---

## Installation and Setup

### Prerequisites

- **C++ Compiler**: GCC or any C++17 compatible compiler.
- **Allegro Library**: Version 5.x installed on your system.
- **Make**: For using the provided Makefile.

### Steps

1. **Clone the Repository**

   ```bash
   git clone https://github.com/username/space-invaders-plus-plus.git
   ```

2. **Navigate to the Project Directory**

   ```bash
   cd space-invaders-plus-plus
   ```

3. **Build the Project**

   ```bash
   make
   ```

4. **Run the Game**

   ```bash
   ./space_invaders_plus_plus
   ```

---

## Usage Instructions

- **Controls**:
  - **Left Arrow / A**: Move left.
  - **Right Arrow / D**: Move right.
  - **Spacebar**: Shoot.
- **Objective**: Destroy all enemies before they reach the bottom of the screen.
- **Pause**: Press **P** to pause the game.
- **Quit**: Press **Esc** to exit the game.
