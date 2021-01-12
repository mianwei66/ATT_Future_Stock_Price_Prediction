# ATT_Future_Stock_Price_Prediction



Stock price predicting is always one of the most important and polular application of time series modeling.

In this study, I'm showing a prediction of future stock price for the top company---AT&T


1.Let's take a look at the dataframe first:

![Screenshot](1.png)

Since the close price of everyday is a key feature for the pracise purpose, it is the value that will be predicted in this study.

Also, the volume as a reflection of outside events, it is a very important variable in my model.

2. Let's take a look at the close price over time:

![Screenshot](2.png)

It is very clear that this time series has a trend. 

By the look of this, there's no clear evidance showing that wether it is a seasonal data or not.

So by calculating the ADF, the P-value is smaller than 0.05. So in our dataset, there is no seasonal affect.

I applied 2 models to this time series: ARIMA and LSTM:

Here are the results for both models:

