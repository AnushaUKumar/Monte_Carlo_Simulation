# Monte Carlo Stock Price Simulation & Portfolio Optimization

## **Overview**

This project uses **Monte Carlo simulations** to predict future stock prices and **optimize investment portfolios** based on risk-adjusted returns. It helps investors analyze uncertainty, expected returns, and efficient stock allocations.

## **Features**

**Monte Carlo Stock Price Simulation** – Predicts future stock prices using historical data and random sampling.\
**Portfolio Optimization** – Identifies the best stock allocation using the **Sharpe Ratio**.\
**Efficient Frontier Visualization** – Compares risk vs. return for different stock portfolios.\
**Risk Analysis** – Computes **confidence intervals & probability estimates** for stock movements.

---

## **Monte Carlo Stock Price Simulation**

We simulate **1000+ stock price paths** using historical daily returns and volatility.

### **Key Steps**

1️ Fetch stock data using `yfinance` 📊.\
2️ Compute **daily returns & volatility**.\
3️ Run **Monte Carlo simulations** to generate **future price paths**.\
4️ Analyze **expected stock price, risk & confidence intervals**.\
5️ Plot simulation results to visualize price uncertainty.

### **Expected Future Price Calculation**

```python
expected_price = simulated_paths[:, -1].mean()
print(f"Expected Future Price: ${expected_price:.2f}")
```

**Helps estimate the most probable stock price at the end of the time horizon**.

---

## **Portfolio Optimization**

We use **Monte Carlo simulations** to find the **best portfolio allocation** of multiple stocks (e.g., AAPL, MSFT, TSLA).

### **Key Steps**

1️⃣ Fetch historical stock data for multiple assets.\
2️⃣ Compute **expected returns & volatility**.\
3️⃣ Simulate **10,000+ random portfolios** with different stock weights.\
4️⃣ Optimize the **Sharpe Ratio** for the best risk-adjusted return.\
5️⃣ Visualize the **Efficient Frontier** (trade-off between risk & return).

### **Optimal Portfolio Weights (Example Output)**

```plaintext
Optimal Portfolio Weights (Highest Sharpe Ratio): [0.3587, 0.4147, 0.2265]
```

Suggests investing **35.87% in AAPL, 41.47% in MSFT, and 22.65% in TSLA** for the best return vs. risk trade-off.

---

## **Visualizations**

### **Monte Carlo Simulations for Stock Price**

- **Plots multiple simulated stock price paths**.
- **Shows uncertainty & probable price range**.

### **Efficient Frontier Chart**

- **Plots risk vs. return for all portfolio combinations**.
- **Marks the best portfolio (⭐) that maximizes Sharpe Ratio**.

---

## **Installation**

Install dependencies:

```bash
pip install numpy pandas matplotlib seaborn yfinance
```

Clone the repository:

```bash
git clone https://github.com/yourusername/monte-carlo-stock-analysis.git
cd monte-carlo-stock-analysis
```

Run Jupyter Notebook:

```bash
jupyter notebook
```

---

## **Next Steps**

Potential Improvements:

- **Compare different stock combinations (e.g., AAPL, GOOG, NVDA)**.
- **Use Machine Learning (LSTM) to predict stock prices**.
- **Backtest portfolio performance on real data**.

---


