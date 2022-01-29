# Neural_Network_Charity_Analysis
Module 20 Neural Network


## Overview of the analysis
In this module we created a binary classifier capable of predicting whether applicant charities would use funds from AlphabetSoup successfully. To predict which charities are worth funding we used deep leaning neural network models with TensorFlow.


## Results

- Data Preprocessing
	- The target variable was the column "IS_SUCCESSFUL". We want to know whether the charity was successful or not.
	- The feature variables used in the model were APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, SPECIAL_CONSIDERATIONS, AND ASK_AMT.
	- Because variables "EIN" and "NAME" are neither target nor feature variables we removed them from the data before creating the models.

- Compiling, Training, and Evaluating the Model
	- Out TensorFlow Keras model used two hidden layers with 50 and 25 nodes, respectively. The model used the Relu activation function.
	- The original model yielded a model accuracy of 0.7315452098846436 which was below the target accuracy of 0.75
	- In my first attempt reduced the nodes in the two hidden layers which lowered the accuracy to 0.7313119769096375. My second attempt added a hidden third layer and used 50, 25, and 15 nodes in the three hidden layers. The second attemp accuracy fell to 0.7264139652252197. My third attempt changed the activation function from Relu to Tanh, increased the node count, and increased the number of epochs from 100 to 130. The model accuracy fell to 0.7295626997947693.

## Summary
After multiple attempts I could not get the accuracy to rise to 0.75 or higher. I believe I could potentially increase the accuracy of the model by applying better preprocessing techniques like binning some more feature variables. I could also continue to try more or less nodes at various numbers of hidden layers and try more or less epochs while training the model.