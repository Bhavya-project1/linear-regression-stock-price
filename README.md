# Linear Regression for Stock-Price Modelling

A Jupyter Notebook project exploring whether a linear regression model can explain and predict equity price movements using historical market data and engineered technical features.

The workflow retrieves historical prices with Yahoo Finance, prepares explanatory variables, fits a linear regression model, compares fitted predictions with observed values, and examines model assumptions.

## Workflow

1. Retrieve historical price data using `yfinance`.
2. Construct and inspect explanatory features, including technical indicators.
3. Fit a linear regression model.
4. Compare actual and predicted values.
5. Evaluate prediction errors and model behaviour.
6. Examine ordinary least squares (OLS) assumptions.

## Instruments

The notebook contains data for Apple (AAPL), Amazon (AMZN), Microsoft (MSFT), Invesco QQQ (QQQ), and the S&P 500 Index (^GSPC). See the notebook for the exact target variable, feature definitions, sample period, and specification.

## Concepts

- Ordinary least squares
- Feature engineering and technical indicators
- Train/test evaluation
- Actual-versus-predicted diagnostics
- Regression assumptions and residual analysis

## Technology

Python · NumPy · pandas · yfinance · Matplotlib · Plotly · scikit-learn / statsmodels

## Run

```bash
pip install numpy pandas yfinance matplotlib plotly scikit-learn statsmodels jupyter
jupyter notebook
```

This repository contains more than one notebook. Execute the larger prediction notebook for the fuller workflow.

## Modelling Considerations

A high in-sample fit does not establish forecasting ability. Financial time series are noisy and non-stationary. A credible evaluation should use chronological splits, prevent look-ahead leakage during feature construction, compare with simple baselines, and report out-of-sample metrics.

This project is an educational exploration and does not establish a profitable trading strategy.

## Disclaimer

For educational purposes only. Not investment advice.
