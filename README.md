# Neural_Network_Charity_Analysis

## Analysis Overview
The purpose of this analysis is to use deep-learning neural networks with the TensorFlow platform to create a binary classifier that is capable of predicting whether applicants will be successful if funded by a charity.

## Results

### Data Preprocessing

- The target for the model is the "IS_SUCCESSFUL" column of the dataset. This signifies if the money invested was used effectively.

- The feauture variables of this model are:
	1.) APPLICATION_TYPE
	2.) AFFILIATION
	3.) CLASSIFICATION 
	4.) USE_CASE
	5.) ORGANIZATION 
	6.) STATUS
	7.) INCOME_AMT
	8.) SPECIAL_CONSIDERATIONS
	9.) ASK_AMT
	
- There were a few variables that could be dropped because they are irrelevent and could cause the system to think its significant.
	1.) EIN because the charity's EIN has no affect on their success or not
	2.) STATUS because all row values were 1

### Compiling, Training, and Evaluating

- In this model there were 2 hidden layers used initially with 80 and 30 neurons respectively. The input data has a sample size of 25,724 and 43 features.
- The output layers is done with a binary classification system. 
- The hidden layers nodes were activated using the ReLu function and the output layers used the Sigmoid function.
- The compiler for the model used "adam" as the optimizer and "binary_crossentropy" for the loss function.
- The model accuracy of 73% unfortunately fell short of the 75% goal. 
- To improve performance of the model I decided to not drop the NAME column and instead converted it into a data point. Than I added a third hidden layer and used "sigmoid" for the activatoin function for the 2nd and 3rd hidden layer
- After doing these optimization steps I was able to achieve an model accuracy score of 78%.

## Summary

The deep learning neural network model did achieve its target goal of 75% minimum accuracy. According to the model if an applicant has:
	1.) Its name appear more thean 8 times 
	2.) The type of applicant is one of these: T3, T4, T5, T6, T10, T9, T7, T10  
	3.) The application has one of these CLASSIFICATION: C1000, C2000, C1200, C3000, C2100
They have a 78% chance of succeeding.

A different model that could be used would be the Random Forest Classifier to combine different decision trees to generate a classified output and compare its performance against this model.
