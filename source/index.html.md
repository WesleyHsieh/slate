---
title: API Reference

language_tabs:
  - python

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Python implementation of policy gradient reinforcement learning methods, built on TensorFlow. Flexible reinforcement learning framework that does not require dynamics of the environment. Given a sequence of state-action pairs and rewards, adjusts policy based on gradient steps with respect to its parameters. 

# Installation
Quick installation using the pip package manager.
<aside class="notice">
Dependencies: NumPy, TensorFlow, Nose
</aside>

> pip install -i https://testpypi.python.org/pypi policy_gradient

# Interface

Quick, clean interface for training a neural network using policy gradient methods.

```python
learner = PolicyGradient(net_dims, 'tanh')
learner.train_agent(dynamics_func, reward_func, initial_state)
learner.get_action(new_state)
```

<aside class="notice">
</aside>

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>
<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

## Main Functions
### train_agent
Parameters:

    dynamics_func: function
      User-provided function that takes in 
      a state and action, and returns the next state.

    reward_func: function
      User-provided function that takes in 
      a state and action, and returns the associated reward.

    initial_state: array-like
      Initial state that each trajectory starts at.
      Must be 1-dimensional NumPy array.

    num_iters: int
      Number of iterations to run gradient updates.

    batch_size: int
      Number of trajectories to run in a single iteration.
      
    traj_len: int
      Number of state-action pairs in a trajectory.

    Output:
    mean_rewards: array-like
      Mean ending rewards of all iterations.

```python
train_agent(dynamics_func)
```
## Utility Functions
asdfadsf