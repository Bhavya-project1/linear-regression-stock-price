# Linear Regression and Lasso for Next-Day Equity Price Modelling

A Jupyter Notebook study of ordinary least squares (OLS) and Lasso regression for modelling the next-day closing price of Apple (AAPL). The workflow uses historical prices for AAPL, AMZN, MSFT, QQQ and the S&P 500 Index as inputs.

## Research Workflow

1. Retrieve daily closing-price data from Yahoo Finance for the 2020–2024 modelling sample.
2. Engineer one-day lag features and five-day moving averages for the selected instruments.
3. Define the next trading day's AAPL closing price as the target.
4. Fit an OLS regression, inspect its summary, and compare a reduced specification using lagged AAPL and S&P 500 prices.
5. Examine regression diagnostics: linearity, residual-versus-fitted behaviour, variance inflation factors, residual normality, and Durbin–Watson statistic.
6. Apply a chronological training/test split for a Lasso regression experiment and report R², MSE, and RMSE.
7. Compare actual and predicted AAPL prices over a 2025 evaluation interval.

## Repository Contents

- Linerar_regression_stock_prediction.ipynb — full prediction workflow (filename retained as it currently exists in the repository).
- Linear_Regression_Stock_Price.ipynb.ipynb — companion notebook.

## Technology

Python · NumPy · pandas · yfinance · Matplotlib · Plotly · statsmodels · scikit-learn · seaborn

## Run

~~~bash
pip install -r requirements.txt
jupyter notebook
~~~

Open the larger prediction notebook and execute cells in sequence. Market data is downloaded at runtime; historical observations and provider adjustments can change.

## Important Evaluation Caveat

Price levels are often highly persistent, so a model can achieve apparently strong price-level fit without forecasting economically meaningful returns. A more rigorous extension should compare against a previous-close naïve forecast, use return or price-change targets, and report chronological out-of-sample MAE/RMSE alongside directional and economic metrics. The exploratory diagnostic comments in the notebook should not be treated as formal proof that every OLS assumption is satisfied.

## Disclaimer

Educational regression-modelling exercise only. It does not establish a profitable trading strategy and is not investment advice.
