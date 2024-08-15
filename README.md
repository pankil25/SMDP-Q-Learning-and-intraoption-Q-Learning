# SMDP-Q-Learning-and-intraoption-Q-Learning

## Overview
This repository contains implementations specifically Single-step Semi-Markov Decision Process (SMDP) Q-learning and intra-option Q-learning, applied to the Taxi-v3 environment from the OpenAI Gymnasium library. 

## Requirements
Make sure you have the following libraries installed:
- `numpy`
- `matplotlib`
- `gymnasium`

You can install them using pip:
```bash
pip install numpy matplotlib gymnasium
```

## Environment Description
The Taxi-v3 environment is a grid-based simulation where a taxi must navigate to pick up and drop off a passenger at designated locations. The environment consists of a 5x5 grid with 500 discrete states, where:
- The taxi can be in any of the 25 positions.
- The passenger can be at one of 5 locations (including in the taxi).
- There are 4 possible drop-off destinations.

### State Representation
- **Passenger Locations**: 
  - 0: Red
  - 1: Green
  - 2: Yellow
  - 3: Blue
  - 4: In taxi
- **Destinations**: 
  - 0: Red
  - 1: Green
  - 2: Yellow
  - 3: Blue

### Rewards
- -1 per step unless a different reward is triggered.
- +20 for successfully delivering a passenger.
- -10 for illegal "pickup" and "drop-off" actions.

The discount factor (γ) is set to 0.9.

## Actions and Options
- **Primitive Actions**:
  - 0: Move South
  - 1: Move North
  - 2: Move East
  - 3: Move West
  - 4: Pick passenger up
  - 5: Drop passenger off

- **Options**: Options are available to move the taxi to each of the four designated locations when the taxi is not already there.

## Tasks
1. Implement Single-step SMDP Q-learning for the taxi problem.
2. Implement Intra-option Q-learning for the same environment.
3. For both algorithms, plot reward curves and visualize the learned Q-values.
4. Provide a written description of the learned policies and reasoning.
5. Explore alternate sets of mutually exclusive options and compare the performance with the original options.

## Code Run:

### Run from cell number 1 to last cell sequencially
