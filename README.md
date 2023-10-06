# Pursuit-evasion-game-with-deep-reinforcement-learning-DDPG

Welcome to the **Pursuit evasion game with deep reinforcement learning (DDPG)** repository! This project focuses on utilizing Deep Deterministic Policy Gradient (DDPG) to solve the classic pursuit evasion problem, where a pursuer aims to capture an evader in a dynamic environment with random motion.

## Overview
A pursuite evasion game (PEG) is a dynamic game between two robots or agents, named the pursuer **p** and evader **e**.  
- **p** tries to catch the evader agent **e** as quickly as possible. 
- **e** on the other tries to avoid capture or at least delay it as long as possible.   

Both agents react to each others actions and try to complete optimal actions to achive their goals.  
This work served as preperation for my master thesis and explore the use of Deep Deterministic Policy Gradient (DDPG).  
DDPG is considered a state of the art deep reinforcement Learning algorithm adapted for problems / games with continuous action domain, such as robotics.  
Usually in Robotics, a kinematic model describes the motion of the robot given its linear and angular velocities.  In other words, we command velocities to reach a defined position.  
It's a continous action domain, since the velocity is a physical variable that belongs to a continuous interval **[Vmin, Vmax]**.

In this work, we will use DDPG to train a pursuer with the goal to catch an evader that has random actions. Both agents have constant speeds but variable angular velocities (steering). **p** will have a speed advantage and **e** will have a steering advantage.

## Implementation
A nice implementation of DDPG is offered on Keras Website :
https://keras.io/examples/rl/ddpg_pendulum/

The main work here is to :
- Define Observations
- Define the transition or step function
- Define a reward model
- Adapt the DDPG model to the problem
- Build the algorithm that trains the pursuer to complete its goal.
- Identify ways to evaluate the results.

## Note
If you want to use this notebook, you need to create the directory 'myddpg', on your local machine, to save the models.