# Neural_Network_Charity_Analysis

## Overview of the analysis: Explain the purpose of this analysis.

The purpose of this analysis was to use features within our dataset to create a binary classifier that is capable of predicting whether charity applicants will be successfuly if funded by Alphabet Soup. More than 34,000 organizations have received funding from Alphabet Soup and the following metadata was captured for each:

- EIN and NAME: Identification columns
- APPLICATION_TYPE: Alphabet Soup application type
- AFFILIATION: Affiliated sector of industry
- CLASSIFICATION: Government organization classification
- USE_CASE: Use case for funding
- ORGANIZATION: Organization type
- STATUS: Active status
- INCOME_AMT: Income classification
- SPECIAL_CONSIDERATIONS: Special consideration for application
- ASK_AMT: Funding amount requested
- IS_SUCCESSFUL: Was the money used effectively

## Results:

After preprocessing our data, our model loss was 0.5679 and our model accuracy was 0.7254:

![image](https://user-images.githubusercontent.com/89496798/155922639-67878e26-5e60-44db-a407-2f1a47bce203.png)

### Data Preprocessing

#### What variable(s) are considered the target(s) for your model?
The variable we took into consideration as the target for our model was if the money was used effectively resulting in a successful charity - This was the IS_SUCCESSFUL parameter within our dataset.

#### What variable(s) are considered to be the features for your model?
The variables that we considered to be the features in our model were the application type, affilition, classification, use case, organization, status, income amount, special considerations, and the ask amount.

#### What variable(s) are neither targets nor features, and should be removed from the input data?
The variables that are neither targets nor features and were removed from our dataset were the identification columns - the EIN and NAME

### Compiling, Training, and Evaluating the Model

#### How many neurons, layers, and activation functions did you select for your neural network model, and why?
For our neural network model, there were a total of 110 neurons and 2 hidden node layers. The activation function used for both layers was the Rectified Linear Unit (Relu) function. This was used because it returns a value from 0 to infinity and because it's the most used activation function in nueral networks due to its simplifying output. The activation function used for our output layer was the Sigmoid function. This was used because it transforms the output to a range between 0 and 1 which will reflect well from our scaled data.

#### Were you able to achieve the target model performance?
Our target model only achieved loss of 0.57 and accuracy of 0.73. Our goal was to achieve accuracy of 0.75.

#### What steps did you take to try and increase model performance?
As an attempt to optimize performance I removed additional variables, added neurons to the hidden layers, added additional hidden layers, and used the sigmoid and tanh activation functions.

## Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.
A logistic regression model may help us acheive our desired accuracy of more than 75% since this type of model is a classification algorithm that can analyze continuous and categorical variables. By using a combination of input variables, logistic regression predits the probability of the input data belonging to one of two groups - in this case, if the charity was successful or not.
