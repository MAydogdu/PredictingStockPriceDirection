# PredictingStockPriceDirection
An investments application of machine learning

July 2017, Murat Aydogdu
This project is in some ways a replication of Liew and Mayster (2017): "Forecasting ETFs with Machine Learning Algorithms"
I look at active stocks whereas they use ETFs. Also, I look at only one frequency: 20-trading day (one month) 
since they report stronger results for 20 day and longer horizons. Also, I use dollar-trading volume and scale trading volume
so that these features are comparable across stocks.

The goal is predicting the price movement (or return) over the next month: whether the stock will move or or not. 
Features used in prediction are: past returns, past volume, and calendar (day of the week and month of the year) variables.

This project consists of two parts:
- Using data from yahoo finance, construct a dataset that includes five tickers (AAPL, GOOGL, AMZN, MSFT, and IBM) 
  and price and volume data for each. Prices are used to compute returns and dollar trading volumes. Past 20-day return, 
  past 20-day average volume and 10 lags of each of these variables are computed for each ticker. This step produces
  a "wide-format" file which has all ticker-price-volume data as well as the lags for each day.

- Performing predictions using three models (Neural Networks, Support vector Machines, and Random Forests) after first 
  finding best metaparameters using a grid search / cross validation approach. The best models are then trained and 
  their performance on test sets are reported.
