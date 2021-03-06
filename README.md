# ATT_Future_Stock_Price_Prediction



Stock price predicting is always one of the most important and polular application of time series modeling.

In this study, I'm showing a prediction of future stock price for the top company---AT&T


# 1.Dataset Overlook

The Dataset that I used are daily data of AT&T stock for the past 36 years, and I download them from Yahoo Finance: https://finance.yahoo.com/quote/T/history?p=T. 
It contains over 9000 rows and five columns which are: Open price, close price, daily high price, daily low price, and volume.

![Screenshot](Image/1.png)

Since the close price of everyday is a key feature for the pracise purpose, it is the value that will be predicted in this study.

Also, the volume as a reflection of outside events, it is a very important variable in my model.


# 2.Data cleaning and EDA
The variable that I'm predicting is close price. 
Here is the historical close price over time(daily for the past 36 years):

![Screenshot](Image/2.png)


# 3. Modeling and Evaluation:
  # ARIMA Model:
  
  It is very clear that the close price is a trend series. 

  After detrend the data, there's no clear evidance showing that wether it is a seasonal data or not.
![Screenshot](Image/3.png)

So I calculated the ADF, the P-value is smaller than 0.05. So in our dataset, there is no seasonal affect.
  
  Then I plot the autocorretion and partial autocorrelation.
  
  ![Screenshot](Image/4.png)
  ![Screenshot](Image/5.png)
  
  I chose to apply (3,1,3) for (p,d,q) to my ARIMA model after tested for AIC socres.
  
  The process of ARIMA modeling can be found here: [ARIMA](https://github.com/mianwei66/ATT_Future_Stock_Price_Prediction/blob/main/Models/ARIMA_MODEL.ipynb)
  
  And the RMSE score for ARIMA is is 3.9038, which is better than the baseline.
  
  # LSTM Model:
  
  When applying LSTM model, I created a few more variables based on the date.
  
   ![Screenshot](Image/6.png)
   
  The process of LSTM modeling can be found here: [LSTM](https://github.com/mianwei66/ATT_Future_Stock_Price_Prediction/blob/main/Models/LSTM_MODEL.ipynb)
  
  the RMSE of LSTM is 0.2605, outperform the ARIMA model and baseline. 
  
  # Prediction using LSTM Model:
  
  ![Screenshot](Image/7.png)
  

  




