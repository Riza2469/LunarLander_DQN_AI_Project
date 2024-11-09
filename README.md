# Deep Q-Learning for Lunar Lander 🚀
This project implements a Deep Q-Learning (DQN) agent that learns to navigate and land the Lunar Lander in the OpenAI Gym LunarLander-v2 environment.

## Overview
The goal of this project is to train a deep reinforcement learning agent to achieve successful landings in a simulated lunar environment. The agent uses the DQN algorithm to learn optimal actions through trial and error, aiming to maximize rewards over time by landing the Lunar Lander safely.

## Project Structure
* **lunar_lander_dqn.ipynb:** Jupyter notebook containing the entire DQN implementation, training loop, and analysis of the agent’s performance.
* **checkpoint.pth:** The trained model weights saved for later evaluation.
* **README.md:** Project documentation and instructions.
* **video.mp4:** Optional video of a trained agent landing (generated after running show_video_of_model).
## Environment
The Lunar Lander environment has a continuous state space with 8 dimensions and a discrete action space with 4 possible actions:

0: Do nothing <br>
1: Fire left engine <br>
2: Fire main engine <br>
3: Fire right engine <br><br>
The agent aims to maximize its reward by successfully landing without crashing.

## Installation
To run this project, ensure you have the following installed:

Python 3.x
OpenAI Gym
PyTorch
Additional dependencies: numpy, torch, imageio, base64, glob, deque, IPython
Install the dependencies with:

`pip install gymnasium torch numpy imageio`
## Usage
Clone this repository:

`git clone https://github.com/your-username/lunar-lander-dqn.git`<br>
`cd lunar-lander-dqn`<br><br>
**Run the Jupyter Notebook:** Open lunar_lander_dqn.ipynb and execute the cells to train and evaluate the agent. You can adjust hyperparameters like learning rate, epsilon, or training episodes as needed.

**Visualize the Trained Agent:** After training, run the show_video_of_model function in the notebook to generate a video of the agent’s performance.

## Key Sections in the Code
* **Agent Initialization:** Defines the DQN structure with local and target networks.
* **Training Loop:** The agent interacts with the environment and learns from experiences stored in a replay buffer.
* **Evaluation:** Generates videos and analyzes the performance of the trained agent.
## Results
After training for 2000 episodes, the agent should be able to land consistently without crashing, achieving an average score of around 200.0 over the last 100 episodes.<br>
#### Sample Training Performance:<br>
**Episode:** 347<br>
**Average Score:** 201.10<br>
The trained model (checkpoint.pth) is saved and can be reloaded to observe the agent's performance.

## Future Improvements
* **Hyperparameter Tuning:** Experiment with the learning rate, epsilon_decay_value, and network architecture.
* **Double DQN:** Implement Double DQN to mitigate overestimation bias.
* **Prioritized Experience Replay:** Add prioritization in replay memory to focus on critical experiences.
## License
This project is open-source and available under the MIT License.
