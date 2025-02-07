# Lunar Lander 

This project contains implementation of the Deep Q-Network (DQN) for solving the Lunar Lander problem from OpenAI gym environment.


The solution is based on a [paper](chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://storage.googleapis.com/deepmind-media/dqn/DQNNaturePaper.pdf) in which the algorithm enabled agents to master Atari games using only raw pixels and scores as inputs. 

A CNN is used as non-linear function approximator to represent the action-values (Q). But neural networks are known to be unstable when represented as action-value function. This is due to correlation between subsequent states, correlation between action-values and target values and a small updates to Q significantly changing the policy. 

The approach overcomes these instabilities using two key ideas:
1. Experience replay, which stores past experiences in a memory buffer and samples experiences randomly for training, breaking correlations.
2. Fixed Q-Target Network, which uses a separate target network to stabilize learning and periodically updates target network weights.

## Notebooks
There are two notebooks `LunarLander.ipynb` and `CNN_experiments.ipynb`. 

In the first one the DQN network is trained to solve the lunar lander problem. There I do experiments with some hyperparameters to see how the network performs and compare it to the random actions.

In the second one I have tried to experiment with the architecture of CNN which is used in DQN.

All explanation and comments to the code and results you can find below the cells with code and plots.