# Deep Reinforcement Learning

## Table of Contents
- [Introduction](#introduction)
- [Environment](#environment)
- [Algorithm](#algorithm)
  - [Neural Network](#neural-network)
  - [A2C Implementation](#a2c-implementation)
  - [Training the Model](#training-the-model)
- [Evaluation](#evaluation)
- [Installation](#installation)
- [Usage](#usage)

## Introduction

> **Reinforcement Learning (RL)** is an approach wherein an agent learns to make sequential decisions by interacting with an environment. The objective is for the agent to maximize the cumulative reward it receives over time.

We use Gym for developing and comparing RL algorithms. The project uses the CartPole environment where a pole must be balanced on a moving cart.

## Environment

The CartPole environment involves balancing a pole on a cart moving along a frictionless track. The goal is to prevent the pole from falling over by applying forces to the cart.

## Algorithm

We implement the Advantage Actor-Critic (A2C) algorithm, which consists of:
- An actor predicting the best action based on the current state.
- A critic estimating the state's value function to measure expected future rewards.

### Neural Network

A simple feed-forward neural network is designed for the actor-critic model.

### A2C Implementation

The A2C algorithm trains both the actor and the critic to improve the policy by updating the actor to increase the likelihood of good actions and the critic to better estimate the value function.

### Training the Model

The model is trained using the CartPole environment, recording the actions, rewards, and values for each step to update the policy.

## Evaluation

The trained agent's performance is evaluated using the `choose_action` method. The evaluation includes rendering and saving a video of the agent's performance.

## Installation

Install the required libraries:

```sh
pip install gym[atari,accept-rom-license]
pip install imageio
pip install torch torchvision torchaudio

## Usage

1. Clone the repository.
2. Install the required libraries.
3. Run the Jupyter notebook or the provided Python scripts to train the agent and evaluate its performance.
