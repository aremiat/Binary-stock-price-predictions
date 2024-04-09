The goal of this project is to predict whether the stock price of tesla will go up or down depending on the data that we have today.

We start off by retreiveing the data using yahoo finance. 

We then add the volatility and calculate returns using np.log, and making sure we shift(-1) to actually use the data that we have today to predict tomorrow.

The volatility was calculated with a rolling window over 20 days. (it can be change)

With our return we create a variable direction that takes the value 1 if the return was positive and 0 if the return was negative.

Then we fill our na with the mean value of the volatility over the period (6.48).

We estimate our logit model, and we split our data with 70/30, 70% for training and 30% for testing.

We shift back the prediction by one to compare with our testing data. 

We use a cut off around 0.49 which corresponds to the number of 1 divided by the number total or direction signal (0+1).

We finally calculate the accuracy in sample of 0. 529
