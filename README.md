# Experiment 1 - MDP Representation

## AIM
To represent a real-world scenario using Markov Decision Process (MDP), where a robot navigates a warehouse to deliver a package while avoiding obstacles.

---

## Problem Statement
This MDP models a robot's navigation through a warehouse. The robot must:
- Start at a defined location.
- Pick up a package from a pickup point.
- Deliver it to a delivery point.
- Avoid obstacles along the way.

---

##  Problem Description
The robot has to make decisions at each step to reach its delivery address with maximum reward and least collisions. The decisions are probabilistic due to possible slippage or uncertain movement outcomes.

---

## State Space
Each state is defined by:
- The robot's current position
- The pickup location of the package
- The delivery location
- The positions of obstacles

---

### Sample State

1. Robot is at position 1

2. Package to be picked up is at position 3

3. Delivery point is at position 6

4. Obstacles are at positions 2 and 4


---

## Action Space
0 -> Stay
1 -> Move Left
2 -> Move Down
3 -> Move Right
4 -> Move Up


---

### Sample Action

0 → 3 → 3 → 1


---

##  Reward Function
- **+1** → Successfully reaches delivery address  
- **0** → Any other move (pickup, start, obstacle)

---

##  Graphical Representation
![Graphical Representation](https://github.com/user-attachments/assets/2726df17-fa19-4748-b1a9-315f221df897)

---

##  Python Dictionary Representation
```python
p = {
    1: {
        0: [(1, 0, 0, False)],
        1: [(1, 0, 0, False)],
        2: [(0.7, 3, 0, True), (0.3, 2, 0, False)],
        3: [(0.3, 2, 0, False), (0.7, 3, 0, True)],
        4: [(1, 0, 0, False)]
    },
    2: {
        0: [(1, 2, 0, True)],
        1: [(1, 2, 0, True)],
        2: [(1, 2, 0, True)],
        3: [(1, 2, 0, True)],
        4: [(1, 2, 0, True)]
    },
    3: {
        0: [(1, 3, 0, False)],
        1: [(1, 3, 0, False)],
        2: [(1, 3, 0, False)],
        3: [(0.98, 4, 1, True), (0.7, 1, 0, False)],
        4: [(0.7, 1, 0, False), (0.98, 4, 1, True)]
    },
    4: {
        0: [(1, 4, 0, True)],
        1: [(1, 4, 0, True)],
        2: [(1, 4, 0, True)],
        3: [(1, 4, 0, True)],
        4: [(1, 4, 0, True)]
    }
}
```
## Output
![image](https://github.com/user-attachments/assets/e59d6b36-8d3a-47ed-84ea-f94e9ad135f5)
## Result
Thus, the MDP representation of the robot navigating from a warehouse to the delivery address—while avoiding obstacles—has been successfully modeled, represented in text, graphically, and programmatically using Python.
