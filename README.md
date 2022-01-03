# Alphabet Soup Charity Neural Network Analysis

## Overview

The purpose of this analysis is to use a neural network to decide which companies should recieve loans from Alphabet Soup. This analysis uses python's TensorFlow library to create, train, and evaluate data gathered from previous loans.

## Results

### Data Preprocessing

After looking at the data, I established that the target variable is the "IS_SUCCESSFUL" column. I then removed the "EIN" and "NAME" columns as they did not offer any relevant data that could help the model perform better. The remaining columns became the features for the model.

### Compiling, Training, and Evaluating the Model

For my first attempt at compiling a neuron network consisted of 8 neurons in the first layer and 6 in the second. Both layers had relu activation functions and the output layer had a sigmoid activation function. I started with these parameters as relu does better with nonlinear data, and two layers allows for a second layer to reweight the inputs from the first layer.

In my second attempt, I removed the "SPECIAL_CONSIDERATIONS" column. I also lowered the threshold for the classification column so that there were more unique values from that column. I also added a third layer with 6 neurons apart of it. 

In my third attempt, I reverted back the threshold for the classification column. I also changed the activation function for the three layers to tanh. I did this to see if it would perform better than the relu function. 

In my fourth attempt, I removed the " STATUS" column. I reverted back to two layers and the relu activation function. Lastly, I changed the neurons to 12 in the first layer and 8 in the second layer. This was to increase the parameters passed from the first layer to the second layer from 54 to 104.

![ASC_more](https://github.com/PSWil/Neural_Network_Charity_Analysis/blob/main/Images/ASC.png)
![ASC_scores](https://github.com/PSWil/Neural_Network_Charity_Analysis/blob/main/Images/ASC_scores.png)

## Summary

After four attempts, I was unable to create a model that could preform a 75% accuracy rating. This is potential becasue I got rid of too many columns, I did not use the correct activation function, or I did not have hte right amount of layers and neurons. These were the main areas I continued the change with little to no improvement. Next time, I would research more about activation functions to make sure that I am always choosing the right one based on the data. 
