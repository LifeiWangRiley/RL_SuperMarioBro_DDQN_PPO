# CSCN8020-23F-Sec1-Reinforcement Learning Programming Project Report

## Reinforcement Learning Approach for Super Mario Bros - Group 1

- **Members:**
  - Lifei Wang
  - Jia Zeng
  - Sudhan Shrestha
- **Instructor:** Mahmoud Mohamed
- **Date:** December 13, 2023

---

### Table of Contents

1. [Introduction](#introduction)
    - [Environment](#environment)
    - [States](#states)
    - [Actions](#actions)
    - [Rewards](#rewards)
2. [Data Processing](#data-processing)
3. [Algorithms](#algorithms)
    - [DDQN](#ddqn)
    - [PPO](#ppo)
4. [Experiments](#experiments)
    - [DDQN Experiments](#ddqn-experiments)
    - [PPO Experiments](#ppo-experiments)
5. [Comparison](#comparison)
6. [Challenges](#challenges)
7. [Future Work](#future-work)
8. [Reference](#reference)

---

## Introduction

This project aims to train a reinforcement learning agent on the Nintendo Entertainment System (NES) version of Super Mario Bros. We employ and compare two algorithms: Double Deep Q-Network (DDQN) and Proximal Policy Optimization (PPO), in the gym-super-mario-bros environment.

### Environment

We utilize the OpenAI Gym environment gym-super-mario-bros for this project. The agent is tasked with completing all 32 stages of Super Mario Bros with just three lives. The environment simulates the gameplay frames, similar to the experience of a human player.
![image](https://github.com/LifeiWangRiley/RL_SuperMarioBro_DDQN_PPO/assets/43443377/105261e7-8596-4d86-8fb5-7508059db8b8)

### States

The state includes various information such as pixel values of the current game screen, agent's position, level details, remaining time, and collected items.

### Actions

The environment offers 256 discrete actions with three lists of actions: RIGHT_ONLY, SIMPLE_MOVEMENT, and COMPLEX_MOVEMENT, simulating various degrees of movement and interaction within the game.

### Rewards

The default reward function promotes moving right as quickly as possible without dying, with modifications to account for game clock differences and death penalties.

---

## Data Processing

We preprocess the game frames by converting them to grayscale, resizing, and normalizing the pixel values to feed into our model effectively.

## Algorithms

### DDQN

We implement the Double Deep Q-Network (DDQN) with online and target networks to reduce overestimation bias, adjusting the learning rate during optimization.

### PPO

Proximal Policy Optimization (PPO) alternates between data sampling and optimizing a surrogate objective function, using clipped probability ratios to ensure moderate policy updates.

---

## Experiments

### DDQN Experiments

We conducted five experiments with DDQN, tweaking settings such as batch size, learning rate, and epsilon. We observed how changes in exploration rate and update interval impact the learning performance.

### PPO Experiments

Three experiments with PPO explored different learning rates, batch sizes, and epsilon values. Adjustments were made to optimize the performance and learning efficiency of the agent.

---

## Comparison

We compared DDQN and PPO based on environment setup, reward schemes, and configuration parameters. Our findings suggest differences in performance stability and efficiency, with PPO showing potential in discovering and exploiting strategies despite its variance.

---

## Challenges

The project faced challenges such as GPU setup, code conversion from Torch to TensorFlow, parameter tuning, and computational resource limitations.

## Future Work

Future projects can build on our findings, focusing on extended training durations and further optimization of the chosen algorithms.

## Reference

- Gym-super-mario-bros. PyPI.
- Amber. (2019). Deep Q-learning, part2: Double deep Q network, (double DQN).
- Schulman, J., et al. (2017). Proximal policy optimization algorithms.

For more details, visit our [GitHub repository](https://github.com/LifeiWangRiley/RL_SuperMarioBro_DDQN_PPO).
