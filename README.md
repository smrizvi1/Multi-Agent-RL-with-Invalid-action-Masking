# Multi-Agent-RL-with-Invalid-action-Masking



This repository contains three different implementations of UAV-enabled NOMA (Non-Orthogonal Multiple Access) communications using Shared Deep Q-Networks, each with a different approach to action masking:

## Implementations

### 1. Basic Implementation
Located in `basic masking/`
- Simple post-prediction action masking using -inf values
- Basic DQN architecture
- Direct Q-value masking after prediction

### 2. Masking after predicting Q-Value
Located in `IAM1/`
- Action masking based on paper approach
- Uses -inf masking after Q-value prediction
- Enhanced state representation
- Modified power allocation schemes

### 3. Masking integrated into the architecture
Located in `IAM2/`
- Action masking integrated into neural network architecture
- Uses binary (0/1) masking through Lambda layer
- Dual input network (state and mask)
- Masking influences training process directly

- ### 4. Attempt on the benchmark MDQN
Located in `MDQN clustering/`
- Based on the paper "Multi-Agent Reinforcement Learning in NOMA-Aided UAV Networks for Cellular Offloading" for benchmarking
- No Action masking 
- Fixed clustering

## Key Differences

### Action Masking Approach
- Basic: Post-prediction -inf masking
- IAM1: Enhanced post-prediction masking with improved state handling
- IAM2: Integrated masking in network architecture

### Neural Network Structure
- Basic: Single input (state) network
- IAM1: Single input with enhanced state representation
- IAM2: Dual input (state and mask) network

### Training Process
- Basic: Masking only affects action selection
- IAM1: Masking affects Q-value updates
- IAM2: Masking is part of the training process

## Project Structure

Each implementation follows the same structure:
```
implementation-folder/
├── src/
│   ├── config/
│   │   └── parameters.ipynb      # (or config file)System parameters
│   ├── models/
│   │   ├── action_masking.ipynb # Action masking implementation
│   │   ├── dqn..ipynb           # DQN implementation
│   │   └── system_model.ipynb  # UAV-NOMA system model
│   └── utils/
│       └── visualization..ipynb  # Plotting functions (if present)
```

## Requirements

- Python 3.8+
- TensorFlow 2.x
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/uav-noma-implementations.git
cd uav-noma-implementations
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

## Key Features

### System Model
- Multiple UAV trajectory optimization
- NOMA power allocation
- Dynamic user clustering
- Channel state aware resource allocation

### DQN Implementation
- Experience replay
- Target network
- Epsilon-greedy exploration
- Action masking for invalid actions

### Training Process
- Episodes with multiple time steps
- Dynamic user movement
- Periodic user clustering
- Performance tracking

## Results

Each implementation generates:
- Throughput plots
- Worst-user rate plots
- UAV trajectories
- Training metrics

Results are saved as:
- Data: `.npy` files
- Plots: `.png` files

## Citations


