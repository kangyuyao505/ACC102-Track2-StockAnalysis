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
WRDS Account
You need a WRDS account with access to the CRSP database. Sign up at https://wrds-www.wharton.upenn.edu

📁 File Structure
text
├── META_2023_daily.csv          # Daily data for the first ticker
├── NVDA_2023_daily.csv          # Daily data for the second ticker  
├── META_vs_NVDA_summary.csv     # Summary statistics
└── META_vs_NVDA_comparison.png  # Comparison chart

💻 Usage
Step-by-Step Instructions
Step 1: Import Libraries and Connect to WRDS
python
import wrds
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np

conn = wrds.Connection()
Step 2: Define Core Functions
Run the function definitions for:

get_company_info_by_ticker() - Retrieves company information using ticker symbol

get_daily_data() - Fetches and processes daily data

plot_comparison() - Generates the comparison charts

Step 3: Enter Tickers
python
ticker1 = input("Enter the first stock ticker: ").strip().upper()
ticker2 = input("Enter the second stock ticker: ").strip().upper()
Step 4-5: Data Retrieval
The tool automatically:

Looks up company information

Retrieves daily data for 2023

Calculates cumulative returns and volatility

Step 6-8: Analysis and Output
Calculates summary statistics

Generates comparison charts

Saves data to CSV files

📊 Output Charts
The tool generates four charts in a 2×2 layout:

Cumulative Return Comparison - Shows the total return growth throughout 2023

20-Day Rolling Volatility - Displays annualized volatility trends

Monthly Average Returns - Compares average returns by month

Market Capitalization - Shows market cap changes over time

📈 Sample Output
Summary Statistics Example (META vs NVDA)
Metric	META	NVDA
2023 Cumulative Return (%)	194.13	239.02
Average Annualized Volatility (%)	36.82	45.23
Maximum Drawdown (%)	-12.97	-18.29
Number of Trading Days	250	250
Sample Chart Output
https://META_vs_NVDA_comparison.png

🔧 Supported Tickers
Common supported tickers include:

Company	Ticker	Company	Ticker
Apple	AAPL	Microsoft	MSFT
Tesla	TSLA	NVIDIA	NVDA
Amazon	AMZN	Meta	META
Google	GOOGL	Netflix	NFLX
AMD	AMD	Intel	INTC
IBM	IBM	Oracle	ORCL
⚠️ Notes
The tool uses a pre-defined permno mapping for reliable ticker lookup

Data is only available for 2023 (can be modified in queries)

WRDS connection requires authentication

The fuzzy search feature helps find similar tickers if exact match fails

🐛 Troubleshooting
Common Issues and Solutions
"Ticker not found"

Check if the ticker is spelled correctly

Try using uppercase letters

Some tickers may have changed (e.g., META used to be FB)

Connection Issues

Ensure you have a valid WRDS account

Check your internet connection

Verify WRDS server status

No Data Returned

Confirm the company was publicly traded in 2023

Check if the ticker is active in CRSP database

📝 License
This tool is for educational and research purposes. Users must comply with WRDS data usage policies.

👥 Author
Developed for financial data analysis and research purposes.

🙏 Acknowledgments
WRDS for providing access to CRSP database

CRSP for maintaining comprehensive stock data
