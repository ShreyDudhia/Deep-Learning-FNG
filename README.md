# Deep Learning 
---
In this assignment, we used deep learning recurrent neural networks to model bitcoin closing prices. One model uses the FNG indicators to predict the closing price while the second model uses a window of closing prices to predict the nth closing price.

To get started:

1. Prepared the data for training and testing.
2. Built and trained custom LSTM RNNs.
3. Evaluated the performance of each model.
---
## Prepared the data for training and testing
For the Fear and Greed model, we used the FNG values to try and predict the closing price. 
For the closing price model, we used previous closing prices to try and predict the next closing price. 
Each model uses 70% of the data for training and 30% of the data for testing.
Applied a MinMaxScaler to the X and y values to scale the data for the model.
Finally, reshaped the X_train and X_test values to fit the model's requirement of samples, time steps, and features. (example: X_train = X_train.reshape((X_train.shape[0], X_train.shape[1], 1)))


---
## Build and train custom LSTM RNNs
In each Jupyter Notebook, we created the same custom LSTM RNN architecture. In one notebook, we fit the data using the FNG values. In the second notebook, we fit the data using only closing prices.
Used the same parameters and training steps for each model. This is necessary to compare each model accurately.


---
## Evaluate the performance of each model
Finally, used the testing data to evaluate each model and compare the performance.
This helps us answering the folowing questions:

Q. Which model has a lower loss?
A. The closing price model had a loss of 0.0055 while the fng index had a loss of 0.0497. Thus we can conclude that model based on closing prices make more accurate prediction on actual values.

Q. Which model tracks the actual values better over time?
A. The closing price model tracks the actual values better over time as one can see how closely the "predicted" overlaps the "real" in the line chart plot.

Q. Which window size works best for the model?
A. Window 2 is a perfect fit as it is easy to visualize several months worth data and also show how much of a tight fit the "real" vs "predicted" is.

