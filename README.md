# Udacity Deep Reinforcement Learning Nanodegree
## Project 1: Navigation

### Introduction

The goal of this project is to use Deep Reinforcement Learning
to train an agent to navigate in a large, square world featuring
blue (bad) and yellow (good) collectible bananas.
The environment the agent deals with was provided by [Udacity](https://www.udacity.com/)
as part of the [Deep Reinforcement Learning Nanodegree Program](https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893)
and is based on the [Unity ML-Agents Toolkit](https://github.com/Unity-Technologies/ml-agents).

#### Rewards

The agent is rewarded as follows:
- **`+1`** when the agent collects a yellow banana
- **`-1`** when the agent collects a blue banana
- **`0`** when the agent is not collecting anything

Since the goal is to maximize cumulative reward (i.e. score)
over an episode (which is a fixed number of steps),
the agent will learn to collect yellow bananas as quickly as possible
while avoiding blue bananas.

#### Actions

The same four discrete actions are available to the agent at all times:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

Note: if the agent is running into a wall, the environment will
simply dismiss the action, but the corresponding action remains available.

#### State

The agent perceives the environment through a state vector that has 37 dimensions.
This state information contains the agent's velocity as well as
ray-based perception of objects around the agent's forward direction
(in other words, the objects in front of the agent).

#### Benchmark goal

An agent will not be deemed sufficiently well-trained if it does not achieve
a score greater than or equal to `+13` (averaged over `100` episodes).

### Setup

To run this project, you first need to install the [Anaconda Distribution](https://www.anaconda.com/distribution/)
including Jupyter Notebook.

In the **Anaconda Prompt**,
create an environment for the project with the following command:
```shell script
conda create --name banana python=3.6
```

Activate the environment with the following command
(prefix it with `source` on Linux):
```shell script
activate banana
```

If you have not done it already, clone this project with the following command:
```shell script
git clone https://github.com/NadCAtarun/banana-catcher.git
cd banana-catcher
```

From the **root folder** of this project,
run the following command
to install the required packages:
```shell script
pip install -r requirements.txt
```

Create an IPython kernel (to use on Jupyter) for the `banana` environment
with the following command:
```shell script
python -m ipykernel install --user --name banana --display-name "banana"
```

Download the Unity environment (supplied by Udacity)
matching your operating system:
- [Linux](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
- [Windows 64-bit](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)
- [Windows 32-bit](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
- [Mac OSX](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)

Unzip it in root folder of the project.

### Usage instructions

From the root folder or one of its parent folders,
launch Jupyter Notebook with the following command:
```shell script
jupyter notebook
```

Open the `Report.ipynb` with the `banana` kernel
and run its cells to train your own agent.
