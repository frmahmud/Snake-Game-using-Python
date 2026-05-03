# 🐍 Snake Game using Python

A classic Snake game built with **Python** and **Pygame**, featuring boundary-wrap mechanics, a real-time scoreboard, and adjustable speed — all in a clean 500×500 grid window.

---

## 📋 Table of Contents

- [Demo](#-demo)
- [Features](#-features)
- [Project Structure](#-project-structure)
- [Prerequisites](#-prerequisites)
- [Installation](#-installation)
- [How to Play](#-how-to-play)
- [Game Mechanics](#-game-mechanics)
- [Architecture](#-architecture)
- [Author](#-author)

---

## 🎮 Demo

> The game runs in a 500×500 pygame window on a 20×20 grid.  
> See `Flowchart of snake game.pdf` and `classDiagram_snakeGame.jpeg` in the repo for design documentation.

---

## ✨ Features

- 🟥 **Boundary-wrap mode** — the snake wraps around screen edges instead of dying on contact
- ⚡ **Adjustable speed** — choose your own difficulty at startup
- 📊 **Live scoreboard** — score updates in real time as you eat food
- 🐍 **Animated snake eyes** on the head segment
- 🔄 **Play Again prompt** — restart without closing the window
- 🧩 **OOP design** — clean class-based architecture (`snake`, `worm`, `scoreboard`)

---

## 📁 Project Structure

```
Snake-Game-using-Python/
│
├── Snake_withboundary.py        # Main game source file
├── Prerequisite                 # Required libraries (plain text)
├── classDiagram_snakeGame.jpeg  # UML class diagram
├── Flowchart of snake game.pdf  # Game logic flowchart
└── README.md                    # Project documentation
```

---

## 🛠 Prerequisites

Make sure you have **Python 3.x** installed, then install the required libraries:

| Library    | Purpose                            |
|------------|------------------------------------|
| `pygame`   | Game window, rendering, input      |
| `tkinter`  | Game-over popup dialog             |

> **Note:** `tkinter` is included in most standard Python installations. `pygame` must be installed separately.

---

## ⚙️ Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/frmahmud/Snake-Game-using-Python.git
   cd Snake-Game-using-Python
   ```

2. **Install Pygame**
   ```bash
   pip install pygame
   ```

3. **Run the game**
   ```bash
   python Snake_withboundary.py
   ```

4. **Enter a speed value** when prompted in the terminal (5–10 recommended).

---

## 🕹 How to Play

| Key          | Action           |
|--------------|------------------|
| `←` Arrow    | Move Left        |
| `→` Arrow    | Move Right       |
| `↑` Arrow    | Move Up          |
| `↓` Arrow    | Move Down        |

- **Eat the green food** to grow longer and increase your score.
- **Avoid hitting yourself** — the game ends if the snake collides with its own body.
- **Boundary wrapping** is enabled: crossing an edge brings the snake out the other side.
- On game over, a popup asks if you want to **play again**.

---

## ⚙️ Game Mechanics

- The game grid is **20×20 cells** on a **500×500 px** window.
- Food spawns randomly, never overlapping the snake's body.
- Score equals the number of body segments minus the initial head (i.e., food eaten).
- Speed is controlled by a `clock.tick(speed)` call — higher value = faster snake.

---

## 🏗 Architecture

The project follows an object-oriented design. Key classes:

### `worm`
Represents a single body segment. Handles position and rendering (including eyes on the head).

### `snake`
Manages the full snake — a list of `worm` segments, directional turns, movement, collision, growth, and reset.

### `scoreboard`
Tracks and renders the current score onto the game surface.

### Helper functions
| Function         | Purpose                                      |
|------------------|----------------------------------------------|
| `drawGrid()`     | Renders the game grid and red boundary lines |
| `randomSnack()`  | Spawns food at a random, unoccupied position |
| `redrawWindow()` | Redraws the full game surface each frame     |
| `message_box()`  | Displays the game-over dialog via tkinter    |
| `main()`         | Entry point — initialises and runs game loop |

For a visual overview, see:
- 📄 [`Flowchart of snake game.pdf`](./Flowchart%20of%20snake%20game.pdf)
- 🖼 [`classDiagram_snakeGame.jpeg`](./classDiagram_snakeGame.jpeg)

---

## 👤 Author

**Firoz Mahmud**  
📧 fmahmud.ruet@gmail.com  
🌐 [frmahmud.github.io](https://frmahmud.github.io)

---

*Created: September 2022*
