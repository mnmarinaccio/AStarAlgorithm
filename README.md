# A* Path Planning for Robotics

This Jupyter Notebook demonstrates the A* path planning algorithm for a grid-based environment with obstacles. It defines a start and goal position and visualizes the shortest path that avoids obstacles using matplotlib.

---

## Table of Contents
1. [Overview](#overview)
2. [Requirements](#requirements)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Examples / Screenshots](#examples--screenshots)
6. [How it Works](#how-it-works)
7. [License](#license)

---

## Overview
The notebook provides a visual demonstration of the A* algorithm:
- Defines a grid with obstacles.
- Sets start and goal positions.
- Computes the shortest path using A*.
- Visualizes the grid, obstacles, start, goal, and final path using matplotlib.

---

## Requirements
- python==3.11.11
- heapq
- matplotlib==3.10.0
- numpy==1.26.4

## Installation
git clone https://github.com/mnmarinaccio/AStarAlgorithm.git <br />
cd AStarAlgorithm

You can install the dependencies with: <br />
pip install -r requirements.txt

## Usage
Open the notebook in Jupyter and run all cells <br />
jupyter notebook AstarPathPlanning.ipynb

## Example / Screenshots
<p float="left">
  <img src="images/path_example_before.png" width="45%" />
  <img src="images/path_example_after.png" width="45%" />
</p>


## How It Works

1. **Grid Definition**
   - The environment is represented as a 2D grid.
   - Obstacles are marked within the grid to indicate blocked cells.
   - Start and goal positions are defined.

2. **A\* Algorithm**
   - The algorithm searches for the shortest path from the start to the goal.
   - It uses a **cost function** (distance from start) and a **heuristic** (estimated distance to goal, e.g., Manhattan distance) to prioritize nodes.
   - Only navigable (non-obstacle) cells are considered for path expansion.

3. **Pathfinding Process**
   - Open and closed lists track explored and unexplored nodes.
   - At each step, the node with the lowest total cost (cost + heuristic) is selected.
   - The algorithm continues until the goal is reached or no path exists.

4. **Visualization**
   - The grid is displayed using **matplotlib**.
   - Obstacles, the start, and goal are clearly marked.
   - The final shortest path is overlaid on the grid for easy visualization.

## License
This project is licensed under the Apache 2.0 License. See the LICENSE file for details.
