# Grid World with SARSA and Q-Learning

## Environment Description

### Grid World Overview
- **Grid Dimensions**: 10x10
- **States**:
  - **Start State**: The initial state of the agent.
  - **Goal States**: The agent aims to reach these (3 goal states).
  - **Obstructed States**: Walls that block entry.
  - **Bad States**: Entering these states incurs a penalty of -6.
  - **Restart States**: Entering these states incurs a penalty of -100 and teleports the agent to the start state.
  - **Normal States**: Default states with a penalty of -1.

### Actions and Transitions
- **Actions**: The agent can move ‘up’, ‘down’, ‘left’, or ‘right’.
- **Stochasticity**:
  - **p**: Probability that the agent moves in the intended direction.
  - **b**: Parameter that defines probabilities of moving to adjacent states if the agent does not move as intended.
- **Wind Effect**: 
  - With a 40% chance, the wind can push the agent one cell to the right after transitioning.

### Rewards
- **Goal States**: +10
- **Restart States**: -100
- **Bad States**: -6
- **Normal States**: -1

## Tasks

### 1. Implement SARSA and Q-Learning

Implement the following Temporal Difference Learning algorithms:
- **SARSA**
- **Q-Learning**

### 2. Conduct Experiments

#### Experimental Setup
- **Start States**: (0, 4) and (3, 6)
- **Grid World Variants**:
  1. **Clear, Deterministic**: No wind, p = 1.0
  2. **Clear, Stochastic**: No wind, p = 0.7
  3. **Windy, Deterministic**: Wind active, p = 1.0

#### Experiment Combinations
- **12 Experiments Total**:
  - 2 Start States
  - 2 Algorithms
  - 3 Grid World Variants

### 3. Determine Optimal Hyperparameters

For each experiment:
- Tune the following hyperparameters:
  - **τ** (softmax) or **ϵ** (ϵ-greedy)
  - **Learning Rate (α)**
  - **Discount Factor (γ)**
- Choose the best action selection policy:
  - **ϵ-greedy**
  - **Softmax**

### 4. Plot Results

For each experiment, generate the following plots:
1. **Reward Curves**: Plot the rewards and the number of steps to reach the goal in each episode.
2. **State Visit Heatmap**: Show the number of visits to each state during training.
3. **Q-Value Heatmap**: Display the Q-values after training and the optimal actions for the best policy.

#### Plotting Details
- **Training**: Train the agent for at least 5000 episodes.
- **Averaging**: Average plots over 5 runs.
- **Reward Curves**: Show the mean and standard deviation.

## Code Running instructions:

#### Run ipynb file from cell number 1 to last cell sequencially.

