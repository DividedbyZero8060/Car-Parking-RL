# Car-Parking-RL

## Overview

This project demonstrates training an autonomous car agent to park in a randomly generated parking slot using reinforcement learning in Unity. The environment is built with Unity and leverages the [Unity ML-Agents Toolkit](https://github.com/Unity-Technologies/ml-agents) for agent training. Training results and analytics are visualized using TensorFlow.

## Project Structure
    ├── .vscode/ # VSCode workspace settings (optional)
    ├── Assets/ # Unity assets: scripts, scenes, prefabs, models
    ├── Logs/ # Unity-generated logs (should be gitignored)
    ├── Packages/ # Unity package manager files
    ├── ProjectSettings/ # Unity project settings
    ├── docs/images/ # Documentation images and figures
    ├── .gitignore # Specifies files/folders to ignore in version control
    ├── README.md # Project documentation (this file)


> **Note:**  
> Folders like `Logs/` and other Unity-generated directories should be excluded from version control using `.gitignore`.

## Environment Description

- **Parking Lot:** The environment consists of a parking area with multiple possible parking slots.
- **Randomization:** Each episode, the parking slot location is randomized to encourage generalization.
- **Agent:** The car agent starts at a random position and orientation. Its goal is to find and park in the designated slot.
- **Obstacles:** Additional parked cars or pedestrians can be included for more complex scenarios.

## Training

- **Toolkit:** Training is performed using Unity ML-Agents, which provides the reinforcement learning framework and communication with Python.
- **Rewards:**
  - Positive reward for successfully parking in the correct slot.
  - Negative rewards for collisions (with other cars, obstacles, or boundaries).
  - Small negative reward per step to encourage efficiency.
- **Observations:** The agent receives information about its position, orientation, velocity, and sensor data (e.g., raycasts for obstacle detection).

## Results & Visualization

- **TensorFlow Integration:** Training progress, reward curves, and agent performance are visualized using TensorFlow dashboards.
- **Evaluation:** After training, the agent's ability to park in various scenarios is demonstrated and can be recorded as videos or images (see `docs/images/`).

## Getting Started

1. **Clone the repository**  
   `git clone https://github.com/DividedbyZero8060/Car-Parking-RL.git`

2. **Open in Unity**  
   Open the project folder in Unity Hub (recommended Unity version: 2021.3 or newer).

3. **Install ML-Agents**  
   Follow the [ML-Agents installation guide](https://github.com/Unity-Technologies/ml-agents) to set up the toolkit in Unity and Python.

4. **Train the Agent**  
   Use the provided training scripts and configuration files to start training:

         mlagents-learn config/your-config.yaml --run-id=CarParking_001

   
5. **Visualize Results**  
Use TensorBoard to visualize training progress:

        tensorboard --logdir results/


## References

- [Unity ML-Agents Toolkit Documentation][3]
- [Autonomous Car Parking Simulator Example][5]
- [Multi-Agent Car Parking RL Example][2]
- [TensorFlow Integration Guide][4]

---

Enjoy experimenting with reinforcement learning for autonomous parking!

