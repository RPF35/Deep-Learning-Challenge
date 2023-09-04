Neural Network Model Report

Overview

This project aims to develop a binary classifier that can predict the likelihood of applicants achieving success if they receive funding from Alphabet Soup. The project will utilize the features present in the given dataset and employ diverse machine learning methods to train and assess the model's performance. The objective is to optimize the model in order to attain an accuracy score surpassing 75%.

Results

Data Prep

The model aims to predict the success of applicants if they receive funding. This is indicated by the IS_SUCCESSFUL column in the dataset which is the target variable of the model. The feature variables are every column other than the target variable and the non-relevant variables such as EIN and names. The features capture relevant information about the data and can be used in predicting the target variables, the non-relevant variables that are neither targets nor features will be drop from the dataset to avoid potential noise that might confuse the model.
During preprocessing, I implemented binning/bucketing for rare occurrences in the APPLICATION_TYPE and CLASSIFICATION columns. Subsequently, I transformed categorical data into numeric data using the one-hot encoding technique. I split the data into separate sets for features and targets, as well as for training and testing. Lastly, I scaled the data to ensure uniformity in the data distribution.

Compiling, Training, and Evaluation 

For my initial model, I decided to include 3 layers: an input layer with 80 neurons, a second layer with 30 neurons, and an output layer with 1 neuron. I made this choice to ensure that the total number of neurons in the model was between 2-3 times the numbers of input features. In this case, there were 43 input features remaining after removing 2 irrelevant ones. I selected the relu activation function for the first and second layers, and the sigmoid activation function for the output layer since the goal was binary classification. I trained the model for 100 epochs and achieved an accuracy score of approximately 72.8%. There was no indication of overfitting or under-fitting.

Optimization Model #1

To optimize the model, I added batch normalization to each level to help stabilize and accelerate training by normalizing the activations of each layer. I trained the model for 100 epochs and achieved an accuracy score of approximately 72.9%, which is a slight improvement. 

Optimization Model #2

For the second attempt to optimize, I added a learning rate (set to .001) to slow the convergence and "early stopping" to prevent overfitting by monitoring the validation loss and stop the training when it begins to increase. After training the model at 100 epochs, it achieved an accuracy of 73.0%

Optimization Model #3

For my final attempt, I used hyper parameter tuning. This process identified the optimal hyper parameters, which include using the tanh activation function, setting 41 neurons for the first layer, and assigning 13, 5, and 4 units for the subsequent layers. After training the model at 50 epochs, it achieved an accuracy score of 73.3%.

Summary

I was unable to get a result at the target accuracy of 75%. Given, the results, I would not use any of the 3 models. Making additional changes to the model such as changing the dropout layers, trying out various activation functions, and adjusting the number of layers and neurons could help to optimize the model and achieving the desired goal of 75% accuracy. 
