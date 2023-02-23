# TIME SERISE/Forecasting Daily Closing Price of Tesla Shares using ARIMA GARCH Modelling and Regression Analysis on Historical Data (2018-2022) 

Introduction and Background

We will try to forecast daily closing price of Tesla shares using data spanning from 2018-09-12 to 2022-05-13. We will be using ARIMA GARCH modelling to make the forecast, by fitting several models and the select the best model out of the rest.
We will also try to fit a regression model to the data in order to see if our variable are influencing Tesla closing price.

Method of choosing Model:  

We first need to transform the data into a time series object. With this we can create a time series model, Autocorrelation Function, and Partial Autocorrelation Function to determine the autoregressive value (p), difference, and moving average. We will first look at the time series model and see if it is stationary or not, if it is stationary, we do need to use a difference function. With this information we can create a few different test models and calculate their Akaike Information Criterion correlated (AICc), and those with the lowest AICc will fit the data the best. We will also use the Auto ARIMA function and to see how its AICc compares to the ones we tested. Finally, we will use the Ljung- Box-lack of fit test to calculate the p-value for the model, if it is greater than 0.05 then we can conclude it fits the data well.
We start by plotting the time series and observe that the data have a non -constant mean and variance, showing non-stationarity of the data. We need to log the data to in order to make it variance constant and take the first seasonal difference of it to solve the issue of non-stationarity. Afterwards, we plotted the ACF and PACF of the logged and differenced data in order to have an idea of how our model would look like. Our aim now is to find an appropriate ARIMA model based on the ACF and PACF.
