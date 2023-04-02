# Automated Trading Systems
This repository contains two machine learning-based trading systems:

## MLBacktester:
A class for the vectorized backtesting of machine learning-based trading strategies (classification).

## StockPredictor:
A class for predicting stock prices using a random forest classifier.

### Requirements
Python 3.x
`Libraries:` yfinance, pandas, numpy, scikit-learn, matplotlib, fxcmpy (for MLBacktester only)

### Installation
1. Clone this repository to your local machine.
2. Install the required libraries using pip:
3. pip install yfinance pandas numpy scikit-learn matplotlib fxcmpy

### Usage
#### MLBacktester
1. Import the MLBacktester class from ml_backtester.py.
2. Create a new instance of the MLBacktester class, passing in the required parameters (symbol, start, end, interval, and ptc).
3. Call the test_strategy method to backtest the trading strategy.
4. Call the plot_results method to plot the performance of the trading strategy.

##### Example usage:
from ml_backtester import MLBacktester

#####  Create a new instance of the MLBacktester class
backtester = MLBacktester(symbol="AAPL", start="2010-01-01", end="2021-01-01", interval="1d", ptc=0.001)

##### Test the trading strategy
backtester.test_strategy()

#####  Plot the results
backtester.plot_results()


#### StockPredictor
1. Import the StockPredictor class from stock_predictor.py.
2. Create a new instance of the StockPredictor class, passing in the required parameters (symbol and n_estimators).
3. Call the predict method to predict the stock prices for a given date range.
4. Call the plot_results method to plot the predicted stock prices.

##### Example usage:
from stock_predictor import StockPredictor

##### Create a new instance of the StockPredictor class
predictor = StockPredictor(symbol="AAPL", n_estimators=100)

#####  Predict the stock prices
predictions = predictor.predict(start="2021-01-01", end="2021-02-01")

#####  Plot the results
predictor.plot_results(predictions)
