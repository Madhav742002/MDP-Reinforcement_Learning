#  Reinforcement Learning for Algorithmic Stock Trading

##  Project Overview

This project implements and compares multiple **Reinforcement Learning (RL)** algorithms for automated stock trading. The trading agents learn to make optimal decisions (Buy, Hold, Sell) based on historical market data and technical indicators. The project progresses from a classical **Q-Learning** agent to advanced **Deep Q-Networks (DQN)** and **Double DQN** architectures, demonstrating the power of deep reinforcement learning in financial applications.

---

##  Key Features

-  **Real-time financial data fetching** using `yfinance` (AAPL stock, 3 years of data)
-  **Technical indicator engineering**: RSI, MACD, Moving Averages (SMA/EMA), Bollinger Bands, Volatility
-  **Custom trading environment** (MDP formulation) with realistic transaction costs and drawdown penalties
-  **Three RL agents** implemented from scratch:
  - Tabular Q-Learning
  - Deep Q-Network (DQN) with Experience Replay & Target Network
  - Double DQN (for reduced overestimation bias)
-  **Comprehensive performance & risk analysis** including:
  - Sharpe Ratio, Sortino Ratio, Maximum Drawdown, Calmar Ratio
  - Beta, Alpha, Win Rate, Profit Factor
-  **Sensitivity analysis** of hyperparameters (transaction cost, learning rate, discount factor)
-  **Rich visualizations**: Training curves, portfolio comparison, risk dashboards, drawdown analysis

---

##  Algorithms Implemented

| Algorithm | Description | Key Features |
|-----------|-------------|--------------|
| **Q-Learning** | Tabular method with state discretization | Simple, interpretable, but limited scalability |
| **DQN** | Deep neural network for Q-value approximation | Experience replay, target network, handles continuous states |
| **Double DQN** | Decouples action selection & evaluation | Reduces overestimation, more stable training |


---

##  Tech Stack

- **Python** – Core programming language
- **TensorFlow/Keras** – Deep learning framework for DQN agents
- **PyTorch** – Alternative DL backend (optional)
- **yFinance** – Yahoo Finance data API
- **Pandas / NumPy** – Data manipulation & numerical computing
- **Matplotlib / Seaborn** – Data visualization

---

##  Getting Started

### Prerequisites

```bash
pip install numpy pandas matplotlib seaborn yfinance tensorflow torch

## Launch the Jupyter notebook:
  jupyter notebook MDP_RL.ipynb

 Sample Results :
Metric	             Q-Learning	  DQN (approximate)
Initial Capital	     $10,000	    $10,000
Final Portfolio Value	$9,626	    $19,610
Total Return	       -3.74%	      ~96%
Sharpe Ratio	       -0.49	      Positive
Maximum Drawdown	    8.85%	      Lower

DQN significantly outperforms classical Q-Learning due to continuous state handling and better function approximation.

The project generates several insightful plots:
  Stock price & trading volume
  Daily returns distribution & volatility
  Training reward & portfolio value curves (per episode)
  Action distribution (Buy/Hold/Sell frequency)
  Cumulative returns comparison (RL vs Buy & Hold)
  Drawdown analysis with maximum drawdown highlight
  Rolling Sharpe Ratio & Beta
  Sensitivity analysis plots for hyperparameters

Risk Metrics Computed :
- Sharpe Ratio
- Sortino Ratio
- Maximum Drawdown (%)
- Calmar Ratio
- Beta (vs Buy & Hold)
- Alpha (Annualized %)
- Win Rate (%)
- Profit Factor
- Average Win / Loss (%)

Sensitivity Analysis
We analyze how key hyperparameters affect performance:

Parameter	           Values Tested
Transaction Cost	   0, 0.001, 0.0025, 0.005, 0.01
Learning Rate	       0.001, 0.005, 0.01, 0.05, 0.1
Discount Factor    	 0.9, 0.95, 0.99, 0.999

Key Learning Outcomes
 State representation matters – Technical indicators provide rich market context.
 Deep RL outperforms tabular methods – DQN handles continuous state spaces effectively.
 Experience replay & target networks are crucial for stable DQN training.
 Double DQN further improves stability by reducing Q-value overestimation.
 Risk metrics are essential – High returns are meaningless without understanding drawdowns and risk-adjusted performance.

References & Inspiration:
 Mnih et al., "Human-level control through deep reinforcement learning" (DQN paper)
 Van Hasselt et al., "Deep Reinforcement Learning with Double Q-learning"
 Sutton & Barto, "Reinforcement Learning: An Introduction"

Contributing:
 Contributions, issues, and feature requests are welcome!
 Feel free to check the issues page.
