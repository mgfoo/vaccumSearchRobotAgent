## 🤖 AI Pathfinding for a Vacuum Cleaning Agent  
**Course:** CMPT 310 – Artificial Intelligence (Winter 2024)  
**Languages & Tools:** Python · Informed Search · Heuristics · A* · Turn Cost Modeling

As part of an AI course project, I built and tested multiple **pathfinding algorithms** for a simulated vacuum robot operating in a 2D grid environment with dirty and blocked rooms. The goal was to help the agent navigate the space and clean all dirty rooms efficiently, under various movement and cost conditions.

### 🔍 What I Implemented
- Completed five classical search algorithms to compute optimal or near-optimal paths:
  - ✅ **Breadth-First Search (Graph-based)**
  - ✅ **Depth-First Search (Graph-based)**
  - ✅ **Uniform Cost Search**
  - ✅ **Greedy Best-First Search**
  - ✅ **A\*** (with and without heuristics)
- Designed the agent to **adapt its strategy** to new dirty room targets as the grid updates dynamically after each clean.
- Implemented a **turn-cost modifier**, where every 90° turn adds movement penalty (50% of a forward move), and integrated it across all search strategies.
- Visualized the **explored area (pink)** and **final path (orange)** after each search run; allowed step-by-step and auto-run mode with delay-based animation.
- Conducted performance evaluation of each search algorithm using:
  - Number of steps
  - Cumulative performance cost
  - Area explored
- Contributed to a report analyzing:
  - The impact of turn-costs on different search strategies
  - How additional movement constraints (e.g., vertical vs. horizontal costs) could be implemented and their tradeoffs

---

### 📁 File Breakdown

| **File**             | **What I Used It For**                                                                                      |
|----------------------|--------------------------------------------------------------------------------------------------------------|
| `searchAlgorithms.py`| Implemented all five search strategies (BFS, DFS, UCS, Greedy, A\*) including support for dynamic goals.     |
| `evaluation.py`      | Wrote logic to track step counts, path costs, and performance metrics used for comparisons and animations.   |
| `gridWorld.py`       | Contained environment generation logic, such as placing dirty and blocked rooms in the grid world.           |
| `agent.py`           | Defined the robot agent’s movement, direction tracking, and response to turn-cost penalties.                 |
| `gui.py`             | Created the visual interface for observing the grid, step progression, and colored paths (explored vs. final).|
| `main.py`            | Served as the main entry point for running simulations and selecting between step-by-step and full-path modes.|
| `romaniaExample.py`  | Used this classical AI example to test early implementations of search functions.                            |

---

> 🚀 **Result:** Built a flexible search simulation environment where the vacuuming agent successfully cleaned dynamically changing targets using multiple search algorithms — all under timed and cost-aware conditions.

