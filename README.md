# Minimal Python Backtesting Engine for Crypto Strategies  

This project implements a **from-scratch backtesting engine in Python** to evaluate trading strategies on historical **Bitcoin OHLCV data** (2018–2025, multiple timeframes). It is intentionally compact but modular, making it easy to extend with custom strategies, execution logic, and risk management.  

---

## 📌 Features  
- **Data Handling**  
  - Reads OHLCV data (15m, 1h, 4h, 1d) and infers bars per year.  
  - Cleans, sorts, and indexes price data with proper datetime handling.  

- **Indicators & Strategies**  
  - Implements **SMA crossover strategy** (long-only).  
  - Easily extendable `Strategy` class interface for custom strategies.  

- **Portfolio & Execution**  
  - Simulates trade execution with **slippage and commission**.  
  - Tracks cash, positions, and equity curve over time.  
  - Generates a full **trade log** (date, type, size, price, PnL).  

- **Performance Analytics**  
  - Computes **Total Return, CAGR, Annualized Return, Volatility, Sharpe Ratio, Max Drawdown**.  
  - Visualizes **Equity Curve, Drawdowns, and Trade Markers** on price series.  
  - Exports results to CSV (`equity_curve.csv`, `trades.csv`).  

---

## 📊 Example Results  

### ✅ Daily (1D) data (2018–2025)  
- **Total Return:** +920%  
- **CAGR:** 35.5%  
- **Annualized Return:** 38.9%  
- **Sharpe Ratio:** 8.78  
- **Max Drawdown:** -54.6%  
- **Trades:** 61  

### ⏱ 4H data  
- **Total Return:** +1,691%  
- **Annualized Return:** 38.3%  
- **Sharpe Ratio:** 1.68  
- **Max Drawdown:** -94.6%  
- **Trades:** 380  

### ⏱ 1H data  
- **Total Return:** +1,590%  
- **Annualized Return:** 1.89%  
- **Sharpe Ratio:** 2.08  
- **Max Drawdown:** -51.3%  
- **Trades:** 1,608  

### ⏱ 15m data  
- **Total Return:** -7.5%  
- **Sharpe Ratio:** 0.21  
- **Max Drawdown:** -64.7%  
- **Trades:** 6,590  

---

## 🚀 Getting Started  

### 1. Clone repo & run backtesting engine(update your strategy)  
```bash
git clone https://github.com/Dixit-529/BackeTesting_Engine_For_Quantitative_Strategy.git
cd backtesting-engine
python backtest.py

