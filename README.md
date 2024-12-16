# 10%_down Strategy Backtest

This project simulates and evaluates a trading strategy using historical stock market data. The goal is to test the strategy's effectiveness in identifying profitable trading opportunities and optimizing performance.

## Strategy Overview

The trading strategy is built around two main concepts: **price drops** and **momentum recovery**. Here’s how it works:

### Key Concepts

1. **Tracking Price Drops**:
   - The strategy monitors the stock's price to identify its **highest high**, which is the maximum price reached so far.
   - It calculates how far the current price has dropped from this highest high (as a percentage).

2. **Setting a Threshold**:
   - A predefined percentage drop (e.g., 10%) is used as a trigger. When the stock price drops by this amount, the strategy considers it a potential buying opportunity.

3. **Using Moving Averages for Timing**:
   - The strategy employs an **Exponential Moving Average (EMA)** to evaluate the stock's momentum.
   - If the stock price shows signs of recovery (i.e., EMA indicates upward momentum), the strategy executes a **buy trade**.

4. **Exiting the Trade**:
   - After entering a trade, the strategy monitors the EMA for signs of weakening momentum.
   - If the momentum fades (EMA starts to decrease), it exits the trade by selling the stock, securing any gains or limiting losses.

5. **Optimizing Returns**:
   - The script tests various percentage drop thresholds to identify the most profitable configuration.
   - It tracks performance metrics, including individual trade profits and overall account balance growth.

## Purpose

This backtesting script allows investors and traders to simulate how this strategy would have performed in the past using historical stock data. By analyzing the results, users can:
- Understand the strategy's strengths and weaknesses.
- Optimize parameters like the percentage drop threshold.
- Decide if the strategy is suitable for live trading.

## Usage

To run the backtest, follow these steps:
1. Prepare a CSV file containing historical stock data with required columns like `Open`, `Close`, `High`, and `Low`.
2. Configure trade parameters such as the percentage drop threshold and initial account balance.
3. Execute the script and review the generated reports, which include detailed trade logs and performance summaries.

## Results

The following graph shows how the equity (account balance) evolved over time as trades were executed. The x-axis represents the number of trades, and the y-axis shows the account balance:

![Equity Graph](image.png)

## Disclaimer

This project is for educational and research purposes only. The performance of the strategy in past data does not guarantee success in live markets. Always exercise caution and perform thorough due diligence before applying any strategy to live trading.
