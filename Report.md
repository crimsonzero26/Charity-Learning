### Deep-learning-Challenge
# Report on the Neural Network Model
#### Charity Funding Predictor 
## Overview:

The purpose of this analysis is to create a tool to help the nonprofit foundation Alphabet Soup select the applicants for funding with the best chance of success in their ventures. With the knowledge of machine learning and neural networks, I have used the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, I received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

•	EIN and NAME—Identification columns

•	APPLICATION_TYPE—Alphabet Soup application type

•	AFFILIATION—Affiliated sector of industry

•	CLASSIFICATION—Government organization classification

•	USE_CASE—Use case for funding

•	ORGANIZATION—Organization type

•	STATUS—Active status

•	INCOME_AMT—Income classification

•	SPECIAL_CONSIDERATIONS—Special consideration for application

•	ASK_AMT—Funding amount requested

•	IS_SUCCESSFUL—Was the money used effectively
## Results
###	Data Processing

o	Drop the non-beneficial ID columns, 'EIN' and 'NAME'.  These two variables should be removed because they are neither targets nor features.

o	Check the number of unique values in each column: application_df.nunique()

o	Choose a cutoff value and create a list of application types /classifications to be replaced

o	Convert categorical data to numeric with `pd.get_dummies`

o	Split our preprocessed data into our features and target arrays: the variable “IS_SUCCESSFUl” is the target, and other variables are the features.

•	Compiling, Training, and Evaluating the Model

o	The first model I built uses the following parameters with low computation time in mind:

	Two hidden layers with 80 and 30 neurons, the activation function of relu for the two hidden layers

	The output layer activation function of sigmoid as the model output with 1 node is binary classification between 0 and 1.

	The model performance is with the accuracy of 72.68%. The loss value of 56% indicates that the model can be further optimized. 
###	The Attempts of Three Optimization