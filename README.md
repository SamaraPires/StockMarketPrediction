# StockMarketPrediction
Prediction of stock market prices using S&amp;P 500 data obtained via Yahoo Finance API  

This project starts by downloading the S&amp;P  500 data using the Yahoo Finance API. We download the data based on the GSPC symbol via the ticker class.
The S&P 500 index, or Standard & Poor's 500, is a very important index that tracks the performance of the stocks of 500 large-cap companies in the U.S.

After this, the data is analyzed and cleaned.
The data has the following parameters:

Open: price when the market opened
High: The Highest price of the stock on that trading day 
Low: The Lowest price of the stock on that trading day 
Close: the closing price of the stock on that trading day 
Date: Date for each day the market was open

This project uses a random forest classifier for training our ML algorithm for the following reasons:

Random forests work by training a bunch of individual decision trees with randomized parameters 
And then averaging the results from those decision trees Because of this process, random forests are resistant to overfitting 
They run linearly and can pick up non-linear tendencies in data 
Hence, it is fit for handling the S&P 500 stock market data

We will create a backtest function with data frames, and each data frame will analyze data from the first x years to predict the price for the x+1 year. By creating a loop, we’ll be generating the predictions for the subsequent years

Then, by concatenating the generated predictions, we will backtest against the S&P 500 data to analyze the actual gap between our predictions and the real directional trend of the stock prices.

After that, we will retrain the model with additional features to improve its accuracy by approximately 10%.

