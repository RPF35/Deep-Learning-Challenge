# Deep-Learning-Challenge
 
Overview

This project aims to develop a binary classifier that can predict the likelihood of applicants achieving success if they receive funding from Alphabet Soup. The project will utilize the features present in the given dataset and employ diverse machine learning methods to train and assess the model's performance. The objective is to optimize the model in order to attain an accuracy score surpassing 75%.


Results

Optimization Model #1

To optimize the model, I added batch normalization to each level to help stabilize and accelerate training by normalizing the activations of each layer. I trained the model for 100 epochs and achieved an accuracy score of approximately 72.9%, which is a slight improvement. 

Optimization Model #2

For the second attempt to optimize, I added a learning rate (set to .001) to slow the convergence and "early stopping" to prevent overfitting by monitoring the validation loss and stop the training when it begins to increase. After training the model at 100 epochs, it achieved an accuracy of 73.0%

Optimization Model #3

For my final attempt, I used hyper parameter tuning. This process identified the optimal hyper parameters, which include using the tanh activation function, setting 41 neurons for the first layer, and assigning 13, 5, and 4 units for the subsequent layers. After training the model at 50 epochs, it achieved an accuracy score of 73.3%.

Summary

I was unable to get a result at the target accuracy of 75%. Given, the results, I would not use any of the 3 models. Making additional changes to the model such as changing the dropout layers, trying out various activation functions, and adjusting the number of layers and neurons could help to optimize the model and achieve the desired goal of 75% accuracy. 
