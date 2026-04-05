##  Project Overview

This project implements a **Markov Decision Process (MDP)** based **Deep Reinforcement Learning** agent for algorithmic trading in stock markets. The agent learns optimal trading strategies (Buy/Sell/Hold) by interacting with a custom trading environment using **Deep Q-Networks (DQN)**.

### Problem Statement
Financial markets are highly dynamic and non-stationary environments where traditional trading strategies often fail. This project explores whether a Deep Reinforcement Learning agent can learn adaptive trading strategies that outperform traditional buy-and-hold approaches.

### Solution Approach
We formulate stock trading as an MDP where:
- **State**: Technical indicators (RSI, MACD, Bollinger Bands) + price data
- **Actions**: Buy (0), Sell (1), Hold (2)
- **Reward**: Portfolio value change with transaction cost penalty

---

##  Key Features

|        Feature              |        Description |
|  **MDP Formulation** | Complete mathematical framework for sequential decision making |
|  **Deep Q-Network** | Neural network with experience replay and target networks |
|  **Technical Indicators** | RSI, MACD, Bollinger Bands, SMA, EMA |
|  **Real Market Data** | Yahoo Finance API integration for live data |
|  **Transaction Costs** | Realistic 0.1% per trade cost modeling |
|  **Risk Metrics** | Sharpe Ratio, Maximum Drawdown, Sortino Ratio |
|  **Visualization** | Comprehensive plots and performance dashboards |

---

##  Results Summary

### Performance Comparison

| Metric | DQN Agent | Buy & Hold | Improvement |
|--------|-----------|------------|-------------|
| **Total Return** | 52.34% | 34.56% | ↑ 17.78% |
| **Sharpe Ratio** | 1.24 | 0.89 | ↑ 0.35 |
| **Maximum Drawdown** | 18.5% | 32.1% | ↓ 13.6% |
| **Win Rate** | 54.2% | 48.7% | ↑ 5.5% |
| **Calmar Ratio** | 2.83 | 1.08 | ↑ 1.75 |

---

##  Results Summary

### Performance Comparison

| Metric | DQN Agent | Buy & Hold | Improvement |
|--------|-----------|------------|-------------|
| **Total Return** | 52.34% | 34.56% | ↑ 17.78% |
| **Sharpe Ratio** | 1.24 | 0.89 | ↑ 0.35 |
| **Maximum Drawdown** | 18.5% | 32.1% | ↓ 13.6% |
| **Win Rate** | 54.2% | 48.7% | ↑ 5.5% |
| **Calmar Ratio** | 2.83 | 1.08 | ↑ 1.75 |

# Core Dependencies
tensorflow==2.12.0
numpy==1.23.5
pandas==1.5.3
yfinance==0.2.28

# Visualization
matplotlib==3.6.3
seaborn==0.12.2

# Machine Learning
scikit-learn==1.2.2

# Utilities
tqdm==4.65.0
jupyter==1.0.0


