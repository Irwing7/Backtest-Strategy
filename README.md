# 📊 Backtesting a Moving Average Strategy for BTC/USD

This project implements a simple **Moving Average Crossover Strategy** to backtest historical BTC/USD price data. It evaluates the strategy's performance using key trading metrics and visualizations.
## 🧠 Strategy Overview

A basic crossover system is used:

- **SMA_10**: Short-term moving average (10-period)
- **SMA_50**: Long-term moving average (50-period)

**Trading Logic**:
- **Buy** when SMA_10 crosses **above** SMA_50
- **Sell** when SMA_10 crosses **below** SMA_50

## ⚙️ Methodology

### 1. Data Preprocessing
- Load historical BTC/USD data from `AP_dataset.csv`
- Convert timestamps to datetime format

### 2. Strategy Implementation
- Identify entry/exit points using crossover signals
- Use full capital ($10,000) for each trade without leverage

### 3. Performance Metrics
- 💼 **Trade Log**: All entries and exits with P&L  
- 📈 **Total P&L**: Cumulative profit or loss  
- 📉 **Max Drawdown**: Largest portfolio drop  
- ✅ **Win Rate**: Percent of profitable trades  

### 4. Visualization
- **Equity Curve**: Portfolio value over time
- **Price Chart**: BTC/USD price with Buy/Sell markers

## 🚀 How to Run

### Step 1: Install Dependencies

```bash
pip install pandas numpy matplotlib
```

### Step 2: Prepare the Dataset
- Place `AP_dataset.csv` in the project directory
- Make sure it has these columns:
  - `time` (timestamp)
  - `CLOSE` (closing price of BTC/USD)

### Step 3: Run the Script

**Option A: Terminal**
```bash
python backtest.py
```

**Option B: Jupyter Notebook**
- Run all cells in `main.ipynb`

## 📌 Outputs

- **Trade Log**: Executed trades and results
- **Performance Report**: Total P&L, Max Drawdown, Win Rate
- **Plots**:
  - BTC/USD chart with Buy/Sell points
  - Equity curve of portfolio

## 💡 Optional Enhancements

- Experiment with different SMA values
- Add transaction fees or slippage
- Implement stop-loss and take-profit logic


