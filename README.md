# Project Description

This project implements a Deep Reinforcement Learning (DRL) agent to control the **Unitree Go2** quadruped, focusing on learning robust locomotion behaviors in a physically simulated environment.

### Key Features
- [ ] **Simulation:**
    - [ ] Utilizes **MuJoCo MJX** (JAX-based) for massively parallel GPU simulation using the official Unitree Go2 Menagerie model. Actuators function as implicit **PD controllers**, with the network predicting target joint angles.
- [ ] **Algorithm:**
    - [ ] Features a **Proximal Policy Optimization (PPO)** implementation, offering both a custom backend and a **TorchRL** integration for algorithmic validation.
- [ ] **Training Stabilization:**
    - [ ] **Normalization:** Online input normalization for high-dimensional observations.
    - [ ] **Action Mapping:** Tanh-based output scaling to $[-1, 1]$, mapped to physical joint limits.
    - [ ] **Optimization:** Implementation of **Gradient Clipping**, **Reward Scaling**, and **Cosine Annealing** with Warm Restarts to ensure numerical stability.
- [ ] **Infrastructure:**
    - [ ] Built with **Hydra** for hierarchical configuration and **MLflow** for detailed tracking of performance and loss metrics. Ensures full reproducibility via fixed random seeds.
- [ ] **Current Status:**
    - [ ] While numerical stability and active exploration have been achieved, **reward convergence** is not yet fully realized (work in progress).
