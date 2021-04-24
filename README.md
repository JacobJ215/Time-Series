# Unit 10—A Yen for the Future

The purpose of this assignment is to test various time-series tool by predicting future price movements in the value of the Japanese Yen versus the U.S dollar.

The Japanese Yen data is pulled from a csv containing pricing information for the Yen dating back to 1979 to 2019.  Data is cleaned and filtered to only include pricing information from 1990 to 2019

The Repo is split between two notebooks. 

1. Time Series Forecasting 
2. Linear Regression


## Time - Series Forecasting

This notebook was deisgned to perform time series analysis and modeling in hopes of determing whether there is any predictable behavior.

Within the time_series_analysis notebook we addressed the following. 

1. Decomposition using a Hodrick-Prescott Filter
2. Forecasting Returns using an ARMA Model.
3. Forecasting the Settle Price using an ARIMA Model.
4. Forecasting Volatility with GARCH.

### Conclusions

Based on the models we have I believe that it would be a good time to buy the Yen. This is because with the ARIMA model we can see that price of the Yen is projected to steadliy increase over time and with the ARMA model we see that return are remaining positive throughout the same time span.

As seen with the GARCH model the risk of is expected to increase. This can be looked at as either a positive or negative, this because some investors and analyst beleive that with greater risk comes bigger return and then vice versa.

Based on the model evaluation I would not feel confident using these models for trading, this is becuae our p-values are too high. If we can consistantly create models where the p-values are < 0.05 than I would consider using the models.

## Linear Regression Forecasting

This notebook was designed to build a Scikit-Learn linear regression model to predict Yen futures returns with lagged Yen futures returns.

Within the regression_analysis notebook we addressed the following. 

1. Data Preparation (Creating Returns and Lagged Returns and splitting the data into training and testing data)
2. Fitting a Linear Regression Model.
3. Making predictions using the testing data.
4. Out-of-sample performance.
5. In-sample performance.

### Conclusion

Our models performs better with out of sample data. We can confirm this by comparing the the root mean squared error between each sample. Since the the out of sample data produced a smaller root mean squared error we can say that the our model performs better with testing data.

