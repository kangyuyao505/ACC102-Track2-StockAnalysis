US Stock Daily Data Analysis Tool

## Overview

This is a Python-based stock analysis tool built in Jupyter Notebook that retrieves daily trading data from the WRDS database. Users can input two stock tickers to fetch their 2023 daily data and perform comprehensive comparative analysis.

## Key Features

### 1. Data Retrieval
- Connect to WRDS database
- Query company information (including PERMNO) by ticker symbol
- Fetch full-year 2023 daily trading data

### 2. Calculated Metrics

| Metric | Description |
|--------|-------------|
| Cumulative Return | Based on daily returns |
| 20-Day Rolling Volatility | Annualized (×√252) |
| Maximum Drawdown | Key risk indicator |
| Market Cap | Price × Shares Outstanding (in millions USD) |

### 3. Visualization

The tool generates a **4-in-1 comparison chart**:

1. **Cumulative Return Comparison** - Full-year performance trend
2. **20-Day Rolling Volatility** - Compare stock volatility patterns
3. **Monthly Average Return** - Bar chart comparing monthly performance
4. **Market Cap Change** - Market capitalization trends over time

### 4. Output Files

| Filename | Content |
|----------|---------|
| `{TICKER}_2023_daily.csv` | Individual daily stock data |
| `{TICKER1}_vs_{TICKER2}_summary.csv` | Core statistical summary |
| `{TICKER1}_vs_{TICKER2}_comparison.png` | Comparison chart image |

## Technology Stack

- **Data Source**: WRDS CRSP Database
- **Core Libraries**:
  - `wrds` - Database connection
  - `pandas` - Data processing
  - `matplotlib` - Data visualization
  - `numpy` - Numerical computing

## Example Results (NVDA vs META)

### 2023 Key Metrics Comparison

| Metric | NVDA | META |
|--------|------|------|
| Cumulative Return | +239.02% | +194.13% |
| Annualized Volatility | 45.23% | 36.82% |
| Maximum Drawdown | -18.29% | -12.97% |
| Trading Days | 250 | 250 |

### Key Findings

1. **Performance**: Both NVDA and META delivered strong returns in 2023, with approximately 239% and 194% cumulative returns respectively

2. **Risk Profile**: NVDA exhibited higher volatility (45.23%) compared to META (36.82%), indicating greater risk exposure

3. **Drawdown Control**: META demonstrated better downside protection (-12.97% vs -18.29%)

## Execution Flow

```
1. Connect to WRDS Database
   ↓
2. Input Two Stock Tickers
   ↓
3. Query Company Information (with fuzzy search support)
   ↓
4. Retrieve 2023 Daily Data
   ↓
5. Calculate Statistical Metrics
   ↓
6. Generate Comparison Charts
   ↓
7. Export CSV Files and Chart Images
```

## Important Notes

- Valid WRDS account credentials required
- Setting up a `.pgpass` file is recommended for simplified login
- Ticker symbols are case-insensitive (automatically converted to uppercase)
- Fuzzy search will suggest similar tickers if an exact match is not found
