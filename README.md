# Swinging Up Acrobot with n-Step Q-Learning


 <div align="center">
    <a href="https://colab.research.google.com/github/reshalfahsi/swinging-up-acrobot/blob/master/Swinging_Up_Acrobot_with_n_Step_Q_Learning.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="colab"></a>
    <br />
 </div>


The Acrobot is a robotic arm with two links vertically suspended against gravity. It is an underactuated robot, and we can only exert torque on its elbow. Our goal is to raise its last link above a specified height indicated by a horizontal line. To fulfill this objective, we can use the n-step Q-learning algorithm, one of the family of TD(n) algorithms. TD(n) is a multi-step extension of TD learning (e.g., Q-learning). In the context of the Acrobot, the n-step Q-learning algorithm learns to select optimal actions (applying torque at the elbow) based on the current state (joint angles and velocities) and the expected future rewards. We could design the reward function to provide positive rewards for reaching the target height and penalties for inefficient movements or exceeding time limits. TD(n) uses the rewards collected over the next n steps plus the discounted Q-value at the n-th step instead of updating the Q-value based on just the immediate reward and the next state’s Q-value (as in TD(0) or the standard TD learning). This multi-step approach allows for better credit assignment over longer horizons, potentially speeding up learning.


## Experiment


A simple experiment has been conducted showcasing Acrobot's movement under the n-step Q-learning policy. It is provided in this [notebook](https://github.com/reshalfahsi/swinging-up-acrobot/blob/master/Swinging_Up_Acrobot_with_n_Step_Q_Learning.ipynb).


## Result

## Reward Curve

<p align="center"> <img src="https://github.com/reshalfahsi/swinging-up-acrobot/blob/master/assets/reward_curve.png" alt="reward_curve" > <br /> A very noisy reward curve in the course of 10201 episodes of Acrobot's training session. </p>


## Qualitative Result


The GIF below displays the movement of Arcbot following the learned policy of the n-step Q-learning.

<p align="center"> <img src="https://github.com/reshalfahsi/rocket-trajectory-optimization/blob/master/assets/qualitative_acrobot.gif" alt="qualitative_acrobot" > <br /> Acrobot's main challenge: set the last link above the horizontal threshold line as quickly as possible. </p>


## Credit


- [Acrobots, Cart-Poles, and Quadrotors](https://underactuated.mit.edu/acrobot.html)
- [Generalization in Reinforcement Learning: Successful Examples Using Sparse Coarse Coding](http://incompleteideas.net/papers/sutton-96.pdf)
- [Acrobot](https://gymnasium.farama.org/environments/classic_control/acrobot/)
- [Reinforcement Learning: Industrial Applications of Intelligent Agents](https://rl-book.com/)
- [n-step reinforcement learning](https://gibberblot.github.io/rl-notes/single-agent/n-step.html)
- [Learning from Delayed Rewards](https://www.cs.rhul.ac.uk/~chrisw/new_thesis.pdf)
- [Crossbar Adaptive Array: The first connectionist network that solved the delayed reinforcement learning problem](https://link.springer.com/chapter/10.1007/978-3-7091-6384-9_54)
- [Asynchronous Methods for Deep Reinforcement Learning](https://arxiv.org/pdf/1602.01783)
- [Incremental Multi-Step Q-Learning](https://link.springer.com/article/10.1007/BF00114731)
- [Understanding Multi-Step Deep Reinforcement Learning: A Systematic Study of the DQN Target](https://arxiv.org/pdf/1901.07510)
- [PyTorch Lightning](https://lightning.ai/docs/pytorch/latest/)
