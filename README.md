# ACC102-Track2-StockAnalysis
XJTLU ACC102 Python Data Project

# US Stock Daily Data Analysis Tool

## 📊 Overview

This tool provides a comprehensive analysis of daily stock data for US-listed companies. It allows users to compare two stocks by analyzing their 2023 daily performance, including cumulative returns, volatility, monthly returns, and market capitalization trends.

## 🚀 Features

- **Ticker-Based Analysis**: Simply enter stock tickers (e.g., AAPL, TSLA, NVDA) - no need to know permno
- **Automatic Data Retrieval**: Fetches daily price, return, and shares outstanding data from WRDS CRSP database
- **Comprehensive Metrics**:
  - Cumulative returns (annualized)
  - 20-day rolling volatility (annualized)
  - Maximum drawdown
  - Monthly average returns
  - Market capitalization trends
- **Visual Output**: Generates a 4-in-1 comparison chart
- **Data Export**: Saves daily data and summary statistics to CSV files

## 📋 Prerequisites

### Required Python Packages

```bash
pip install wrds pandas matplotlib numpy
