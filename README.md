# Deep Q-Learning for Lunar Lander

This project trains an agent to safely land a spacecraft in the `LunarLander-v3` environment using Deep Q-Learning (DQN). It’s built with PyTorch and Gymnasium, and the notebook walks through every step — from environment setup to training, saving models, and visualizing results.

---

##  Features

- DQN with separate **local** and **target** Q-networks  
- **Experience Replay** buffer and minibatch sampling  
- **Epsilon-greedy** exploration with decay  
- **Soft updates** for the target network  
- Model checkpoint saving  
- Utilities to record agent runs as GIF or MP4  
- Self-contained notebook (can be modularized into `src/`)

---

##  Files Included

| File / Folder | Description |
|----------------|-------------|
| `Lunar_Landing.ipynb` | Main Jupyter notebook with code, explanations, and visualizations |
| `README.md` | Project overview and usage instructions |
| `requirements.txt` | Python dependencies for setup |
| `.gitignore` | Ignore rules for notebooks, venv, and artifacts |
| `checkpoints/` | Folder for saved model weights (not committed) |
| `results/` | Folder for training plots and demo runs |

---

##  Key Hyperparameters

| Parameter | Value |
|------------|--------|
| learning_rate | 5e-4 |
| minibatch_size | 100 |
| gamma (discount factor) | 0.99 |
| replay_buffer_size | 100,000 |
| tau (soft update) | 1e-3 |
| epsilon_start | 1.0 |
| epsilon_end | 0.01 |
| epsilon_decay | 0.995 |

---

##  Installation and Setup

### 1. Create and activate a virtual environment

```bash
python -m venv venv

# Linux / macOS
source venv/bin/activate

# Windows PowerShell
venv\Scripts\Activate.ps1

