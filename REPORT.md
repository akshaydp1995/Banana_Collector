## Instructions

- To train your own agent, run all cells of notebook `Navigation.ipynb`.

> NOTE - Change path of `file_name` variable in both notebooks to reflect your Unity Environment files.
```
env = UnityEnvironment(file_name= < YOUR UNITY ENV PATH HERE >)
```

## Algorithm

![dqn](https://github.com/akshaydp1995/Banana_Collector/blob/master/assets/dqn.png)

**Deep Q Network** (DQN) is a reinforcement learning algorithm that approximates action-value functions by using neural networks as non-linear function approximators. DQN as achieved state-of-the-art performance on many reinforcement learning tasks, which were previously unachievable with traditional RL algorithms either due to infinite state-space or infinite action-space or both.

DQN doesn't require any additional knowledge about the task it's learning to perform. It takes in **state information** as input and outputs **probabilities** of taking each possible action in that state (in case of discrete action-space) or **continuous action values** (in case on continuous action-space).

- This project repository uses **DQN** algorithm to solve Unity's Banana Collector environment.

- The network architecture used is a simple, fully-connected neural network with 2 hidden layers of sizes, 64 and 128 units. Model definition can be found in `model.py` file.

- Hyperparameter values chosen are as follows :

| Hyperparameter | Value |
| -------------- | ------ |
| LR | 5e-4 |
| GAMMA | 0.99 |
| BUFFER_SIZE | 1e5 |
| BATCH_SIZE | 64 |
| TAU | 1e-3 |
| UPDATE_EVERY | 4 |
| SEED | 0 |
| HIDDEN_LAYERS | [64, 128] |
| DEVICE | GPU |

## Rewards Plot

Rewards obtained by agent plotted as function of episodes of training is shown below :

![rewards_plot](https://raw.githubusercontent.com/akshaydp1995/Banana_Collector/master/assets/rewards.png)

Orange line represents a rolling mean of rewards for latest 100 episodes.
