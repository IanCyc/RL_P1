In this branch we have provided solutions to the Frozen_Lake problem.
It is a small game regarding maze navigation.

Background: 
A robot was abandoned in a frozen world composed of 4x4 grids.
There are four types of grids: Start(S), Ice(F), Hole(H), Destination(G). And each grid has an index from 0 to 15.
The robot will start from S, and reach G to get energy as reward.
When the robot step on H or G, the environment will be reset, and the robot will restart from S.
The robot must collect enough energy to send an SOS signal.
We need design an algorithm to help robot explore the environment and collect energy efficiently.

Environment:
import gym
env is class DiscreteEnv
We have two kinds of environment:
1. env = gym.make('Deterministic-4x4-FrozenLake-v0')
    no other constraints
2. env = gym.make('Stochastic-4x4-FrozenLake-v0')
    The Ice(F) in this environment is slipped, and the robot has 1/3 chance moving to right direction, and 2/3 chance moving to vertical direction(1/3 left & 1/3 right).

We can change environment set and compare the performance between Policy iteration and Value iteration.
