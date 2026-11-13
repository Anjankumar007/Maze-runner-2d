# 🏃 Maze Runner 2D

> A 2D browser game featuring real-time **A\* pathfinding**, autonomous **enemy AI**, and **procedural grid navigation** — built with Vanilla JS and powered by Vite.

---

## 🎮 Overview

Maze Runner 2D is a browser-based game where the player navigates a procedurally generated grid maze while being pursued by an autonomous AI enemy. The enemy uses a live A\* pathfinding algorithm to recalculate the optimal route toward the player in real time.

---

## ✨ Features

- **Real-Time A\* Pathfinding** — Enemy AI recalculates the shortest path to the player every game tick using the A\* algorithm with heuristic navigation
- **Autonomous Enemy AI** — Enemies track and chase the player through the maze with no scripted paths
- **Procedural Grid Navigation** — Maze layout is grid-based, with walls, paths, and entities all operating on a consistent tile coordinate system
- **Modular Architecture** — Clean separation of concerns across engine, entities, pathfinding, maps, and objects
- **Vite-Powered Dev Server** — Fast HMR (Hot Module Replacement) development environment with TypeScript support

---

## 🗂️ Project Structure

```
maze-runner-2d/
├── src/                  # Source assets / additional modules
├── index.html            # Game entry point (HTML canvas host)
├── engine.js             # Core game loop, rendering, and input handling
├── entities.js           # Player and enemy entity definitions and logic
├── pathfinding.js        # A* pathfinding algorithm implementation
├── maps.js               # Maze grid data and map layout definitions
├── objects.js            # In-game object definitions (walls, tiles, items)
├── metadata.json         # Game configuration and metadata
├── package.json          # Project dependencies and scripts
├── vite.config.ts        # Vite bundler configuration
├── tsconfig.json         # TypeScript compiler configuration
├── .env.example          # Environment variable template
└── .gitignore
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Language | JavaScript (ES6+) |
| Build Tool | [Vite](https://vitejs.dev/) |
| Type Safety | TypeScript (`tsconfig.json`) |
| Rendering | HTML5 Canvas (via `engine.js`) |
| Pathfinding | Custom A\* implementation (`pathfinding.js`) |
| Environment | Node.js |

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) v16+
- npm or yarn

### Installation

```bash
# Clone the repository
git clone https://github.com/Anjankumar007/Maze-runner-2d.git

# Navigate into the project directory
cd Maze-runner-2d

# Install dependencies
npm install
```

### Environment Setup

Copy the example env file and configure as needed:

```bash
cp .env.example .env
```

### Running Locally

```bash
# Start the development server
npm run dev
```

Open your browser and navigate to `http://localhost:5173`

### Build for Production

```bash
npm run build
```

---

## 🕹️ How to Play

| Action | Key |
|---|---|
| Move Up | `W` / `↑` |
| Move Down | `S` / `↓` |
| Move Left | `A` / `←` |
| Move Right | `D` / `→` |

> Navigate the maze and reach the exit before the AI enemy intercepts you.

---

## 🧠 Pathfinding Algorithm

The enemy AI is powered by the **A\* (A-Star)** search algorithm implemented in `pathfinding.js`. It uses:

- A **heuristic function** (Manhattan distance) to estimate cost to the goal
- An **open/closed list** to efficiently explore the grid
- Real-time recalculation each game tick to respond dynamically to player movement

The result is an enemy that always finds the optimal route through the maze walls to reach the player.

---

## 📐 Architecture Notes

| File | Responsibility |
|---|---|
| `engine.js` | Main game loop, canvas rendering, input events |
| `entities.js` | Player and enemy state, movement, collision |
| `pathfinding.js` | A\* algorithm, grid traversal, path computation |
| `maps.js` | Grid/map data, tile type definitions |
| `objects.js` | Walls, collectibles, interactive objects |

---


---

## 🙋 Author

**Anjankumar007** — [GitHub](https://github.com/Anjankumar007)
