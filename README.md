# 🐦 Flappy Bird AI using Deep Q-Learning (DQN)

A Reinforcement Learning project in which an AI agent learns to play Flappy Bird autonomously using a Deep Q-Network (DQN) implemented with PyTorch.

## 📌 Project Overview

This project uses Deep Q-Learning to train an AI agent to play Flappy Bird through trial and error.

The agent observes the current game state, selects an action, receives rewards from the environment, and learns from previous experiences to improve its gameplay over time.

## 🧠 Reinforcement Learning Concepts Used

* Deep Q-Network (DQN)
* Q-Learning
* Experience Replay
* Target Network
* Epsilon-Greedy Exploration
* Exploration vs Exploitation
* Neural Network Optimization

## 🔄 Agent Workflow

```text
Environment
     ↓
Observe State
     ↓
Select Action
     ↓
Receive Reward
     ↓
Store Experience
     ↓
Sample Mini-Batch
     ↓
Train DQN
     ↓
Update Target Network
```

## 🏗️ Project Architecture

The agent uses two neural networks:

### Policy Network

The Policy Network predicts Q-values for available actions and is trained during the learning process.

### Target Network

The Target Network calculates stable target Q-values and is periodically synchronized with the Policy Network to improve training stability.

## 🎯 Epsilon-Greedy Strategy

The agent balances exploration and exploitation using an epsilon-greedy strategy.

* High epsilon → More random actions and exploration
* Low epsilon → More actions based on learned Q-values

The epsilon value gradually decreases during training.

## 🧠 Experience Replay

The agent stores previous experiences in Replay Memory:

```text
(State, Action, Next State, Reward, Terminated)
```

Random mini-batches are sampled from the replay memory to train the DQN. This helps improve training stability and reduces the correlation between consecutive experiences.

## 🛠️ Technologies Used

* Python
* PyTorch
* Gymnasium
* Flappy Bird Gymnasium
* PyYAML
* Deep Learning
* Reinforcement Learning

## 📂 Project Structure

```text
flappy-bird-dqn-reforcement-learning
│├── game_flappy_bird.py
├── agent.py
├── dqn.py
├── experience_replay.py
├── parameters.yaml
├── requirements.txt
├── README.md
└── .gitignore
```

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/shravan9102/flappy-bird-dqn-reinforcement-learning.git
```

Navigate to the project directory:

```bash
cd flappy-bird-dqn
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

## 🚀 Training

Run the following command:

```bash
python agent.py <parameter_set> --train
```

Replace `<parameter_set>` with the parameter name defined in `parameters.yaml`.

## 🎮 Testing

To test the trained model:

```bash
python agent.py <parameter_set>
```

The trained model will be loaded and the AI agent will play Flappy Bird automatically.

## 📊 Training Process

1. The agent observes the current game state.
2. An action is selected using the epsilon-greedy strategy.
3. The environment returns the next state and reward.
4. The experience is stored in Replay Memory.
5. A random mini-batch is sampled from the memory.
6. The Policy Network is trained using the sampled experiences.
7. The Target Network is periodically synchronized with the Policy Network.
8. The best-performing model is saved.

## 🔮 Future Improvements

* Implement Double DQN
* Implement Dueling DQN
* Add Prioritized Experience Replay
* Add training reward graphs
* Add gameplay video or GIF
* Improve the neural network architecture

## 👨‍💻 Author

**Shravan Kumar**

M.Tech Computer Science | AI/ML

Interested in Data Science, Machine Learning, Deep Learning, Reinforcement Learning, NLP, and Generative AI.
