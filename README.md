# Portfolio Optimization and Analysis

## Overview
This project focuses on analyzing historical stock data, calculating correlations, variances, and optimizing a portfolio consisting of selected stocks. It involves downloading stock price data, generating covariance and correlation matrices, simulating portfolios, and finding the optimal portfolio based on user-specified risk levels.

## Project Structure

### Key Functions

1. **Data Fetching**:
    - `fetch_stock_prices(start_date, end_date, symbols)`: Downloads historical stock prices for the specified symbols and date range.

2. **Correlation and Covariance Analysis**:
    - `calculate_correlation(prices)`: Computes the correlation matrix for the provided stock prices.
    - `calculate_covariance_matrix(prices)`: Computes the covariance matrix based on log-transformed stock returns.

3. **Stock Pair Analysis**:
    - `find_closest_to_zero_correlation(prices)`: Identifies the pair of stocks with a correlation closest to zero.

4. **Portfolio Metrics**:
    - `calculate_variance(portfolio_prices)`: Calculates variance for each stock in the portfolio.
    - `calculate_std_dev(variance)`: Computes the standard deviation from the variance.

5. **Portfolio Simulation**:
    - Simulates 1000 portfolios with random weights to determine optimal portfolios based on returns and volatility.

6. **User-Specific Portfolio Optimization**:
    - `get_highest_return_asset(portfolios, target_risk, tolerance)`: Finds the portfolio with the highest return for a given risk level or suggests nearby risk levels if none match the user’s input.

### Key Steps

1. **Data Collection**:
    - Download historical stock data for selected symbols (e.g., AAPL, KO, NKE, TSLA) using Yahoo Finance.
    - Segment data into yearly intervals from 2015 to 2020.

2. **Analysis**:
    - Generate correlation and covariance matrices for each year.
    - Identify the optimal stock pair with minimal correlation for portfolio creation.

3. **Portfolio Simulation**:
    - Generate random portfolios with varied weights for selected stocks.
    - Calculate returns and volatilities for each portfolio.
    - Plot the portfolios on a Returns vs. Volatility graph.

4. **User Interaction**:
    - Accept user input for desired risk level.
    - Provide the portfolio with the highest return for the specified risk level.
    - Suggest alternative risk levels if the exact match isn’t found.

5. **Output**:
    - Portfolio metrics including returns, volatility, and asset weights.
    - Expected return for the highest-return portfolio.

## Prerequisites

1. Python 3.8+
2. Libraries:
    - `yfinance`
    - `pandas`
    - `numpy`
    - `matplotlib`

Install dependencies using:
```bash
pip install yfinance pandas numpy matplotlib
```

## Running the Project

1. **Set Up**:
    - Ensure all required libraries are installed.
    - Replace `symbols` in the script with the desired stock ticker symbols.

2. **Execution**:
    - Run the script to:
        - Fetch and analyze stock data.
        - Calculate portfolio metrics.
        - Simulate portfolios and plot results.
    - Input your desired risk level when prompted.

3. **Outputs**:
    - Correlation and covariance matrices for each year.
    - Optimal portfolio details for the specified risk level.
    - Scatter plot of simulated portfolios.

## Example Results

### Correlation and Covariance Matrices
The script prints these matrices for each year (2015-2020) for the selected stocks.

### Optimal Portfolio
Example:
```
For a risk level of 15.0%, the portfolio with the highest return is:
Returns: 0.12
Volatility: 0.15
AAPL_Weight: 0.60
TSLA_Weight: 0.40
```

### Portfolio Expected Return
Example:
```
The expected return for the portfolio with the highest return is: 0.1250
```

## Visualization
A scatter plot of simulated portfolios (Returns vs. Volatility) helps visualize the risk-return trade-off.

## Future Improvements
1. **Expand Asset Universe**:
    - Include more stocks for broader diversification.
2. **Advanced Optimization**:
    - Implement Sharpe ratio optimization.
3. **User Interface**:
    - Develop a GUI or web interface for better user experience.


