# Deep Reinforcement Learning for Distribution System Reconfiguration

## Intro
This is a project for ECE-GY 7123 Deep Learning between Panayiotis Christou, Md. Zahidul Islam and Syed Mohammed Ali Hussaini. Deep reinforcement learning has been used in many settings to learn through trial and error how to effectively capture a policy and perform a specific task like playing games and it has had amazing results like for example beating the world champion in Go or the world champion of Starcraft. Deep RL has found its way in many other applications and in this project we examine its potential in power source distribution reconfiguration in times when the network has reduced functionality.

## Description

## How to Run
Detailed instructions for running the codes are added in two notebooks, which are run_normal.ipynb and run_post_fault.ipynb to reconfigure the system during normal and post-disaster conditions, respectively. The other files including DGs, DSS_CircuitSetup, DSS_Initialize, ieee34Mod1, IEEELineCodes, openDSSenv34, state_action_reward, switch are related to the RL environment settings. Tensorboard is required to view the figures after the simulation. As the OpenDSS software is supported on Windows PC, this repo requires windows PC to run. Python 3.8.10 is used for the simulation. The additional required python libraries are added as requirements.txt.

## Solution Approach
This repository implemented three deep reinforcement learning (RL) algorithms (i.e., PPO, A2C, TRPO) to reconfigure power distribution systems to maximize load supply during disasters. This repo uses the IEEE 34 test system as an environment to be used with the RL algorithms. The environment is obtained from the repo: https://github.com/Jubeyer/RL-to-Reconfigure-Microgrid. A few modifications are made. Specially, a Convolution Neural Network (CNN) is added as a feature extractor. Comprehensive simulation cases are performed in both normal and post-disaster conditions. Additonally, A2C and TRPO algorithms are tested along with PPO. 

## Value of Solution


## Results
















