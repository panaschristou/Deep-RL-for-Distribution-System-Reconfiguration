# Deep Reinforcement Learning for Distribution System Reconfiguration

## Intro
This is a project for ECE-GY 7123 Deep Learning between Panayiotis Christou, Md. Zahidul Islam and Syed Mohammed Ali Hussaini. The report is available [here](https://github.com/panaschristou/Deep-RL-for-Distribution-System-Reconfiguration/blob/main/Deep%20Reinforcement%20Learning%20for%20Microgrid%20Reconfiguration.pdf). Deep reinforcement learning has been used in many settings to learn through trial and error how to effectively capture a policy and perform a specific task like playing games and it has had amazing results like for example beating the world champion in Go or the world champion of Starcraft. Deep RL has found its way in many other applications and in this project we examine its potential in power source distribution reconfiguration in times when the network has reduced functionality.

## Description
In this project we examine different reinforcment learning algorithms (i.e., PPO, A2C, TRPO) in deep reinforcement learning using 3 different neural network archetypes (shallow FC, deep FC, CNN) to find the optimal policy to ensure power distribution through a microgrid with reduced functionality (i.e. broken switches) by finding the most optimal switch configuration. We examine the reward over time for all possible combinations as well as compare the wasted load and the achieved loss.

## How to Run
Detailed instructions for running the codes are added in two notebooks, which are run_normal.ipynb and run_post_fault.ipynb to reconfigure the system during normal and post-disaster conditions, respectively. The other files including DGs, DSS_CircuitSetup, DSS_Initialize, ieee34Mod1, IEEELineCodes, openDSSenv34, state_action_reward, switch are related to the RL environment settings. Tensorboard is required to view the figures after the simulation. As the OpenDSS software is supported on Windows PC, this repo requires windows PC to run. Python 3.8.10 is used for the simulation. The additional required python libraries are added as requirements.txt.

## Solution Approach
This repository implemented three deep reinforcement learning (RL) algorithms (i.e., PPO, A2C, TRPO) to reconfigure power distribution systems to maximize load supply during disasters. This repo uses the IEEE 34 test system as an environment to be used with the RL algorithms. The environment is obtained from the repo: https://github.com/Jubeyer/RL-to-Reconfigure-Microgrid. A few modifications are made. Specially, a Convolution Neural Network (CNN) is added as a feature extractor. Comprehensive simulation cases are performed in both normal and post-disaster conditions. Additonally, A2C and TRPO algorithms are tested along with PPO. 

## Value of Solution
We examine the use of deep neural networks as optimal action function approximators and their usage in a real life application. Deep neural networks could speed up the time to respond in reinstating power back to the whole grid after a natural disaster and could learn more complex functions that will allow to respond to unpredictable situations.

## Results
The performance analysis under different load conditions revealed PPO’s robustness, especially under lower load scenarios, with TRPO outperforming in scenarios with deeper feature extraction networks. The comprehensive fault
analysis further underlined PPO’s adaptability, demonstrating effective load management capabilities across a spectrum of fault conditions. The learning curves for the PPO and A2C algorithms offer insights into the learning dynamics over numerous training steps. PPO’s learning trajectory, characterized by its variance in rewards, indicates its explorative learning strategy and potential for optimizing decision-making in real-time power distribution. Conversely, the A2C algorithm showcased a trend towards stability, albeit with a gradual convergence to a lower reward plateau, implying a need for further tuning to enhance its performance under the complex conditions presented by electrical grid disruptions. The neural network depth analysis revealed a critical insight: a medium-depth network strikes the optimal balance between complexity and performance, providing a guiding principle for designing neural network architectures in reinforcement learning applications for power grid management. Additionally, the use of two different feature extractor networks help to understand the best-suited deep neural network for the reconfiguration task.















