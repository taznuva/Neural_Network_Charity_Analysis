# Neural_Network_Charity_Analysis

## Overview of the analysis: 
With the knowledge of machine learning and neural networks, I'll use the features in the provided dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. The model is considered successful if the accuracy score is more than 75%. 

Within this dataset are a number of columns that capture metadata about each organization, such as the following:

  - EIN and NAME—Identification columns
  - APPLICATION_TYPE—Alphabet Soup application type
  - AFFILIATION—Affiliated sector of industry
  - CLASSIFICATION—Government organization classification
  - USE_CASE—Use case for funding
  - ORGANIZATION—Organization type
  - STATUS—Active status
  - INCOME_AMT—Income classification
  - SPECIAL_CONSIDERATIONS—Special consideration for application
  - ASK_AMT—Funding amount requested
  - IS_SUCCESSFUL—Was the money used effectively

## Results:
Using bulleted lists and images to support your answers, address the following questions.

### Data Preprocessing
- What variable(s) are considered the target(s) for your model?

  The "IS_SUCCESSFUL" is the target for this model since the purpose is to predict whether applicants will be successful.

- What variable(s) are considered to be the features for your model?

  Rest of the columns (excluding 'EIN','NAME', and 'IS_SUCCESSFUL') are considered to be the features for this model. The values have been converted using One Hot Encoding module for the model to comprehend 'object' types. 

- What variable(s) are neither targets nor features, and should be removed from the input data?
  
  The 'EIN' and 'NAME' columns were dropped from the dataframe since it only adds more noise to the model. 


### Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
  2 Layers for 100 epochs using ReLu and Sigmoid activation functions since it had the closest accuracy score to 75%. 
    Layer 1 - 80 neurons
    Layer 2 - 30 neurons
  

- Were you able to achieve the target model performance?

  For the 'AlphabetSoupCharity_Optimization.ipynb' file, I was unable to achieve the target model performance. However, for the 'AlphabetSoupCharity.ipynb'     had better accuracy results (0.70). 

- What steps did you take to try and increase model performance?
  
  To increase model performance, I tried to add layers, add more neurons, and try a different model (tanh)--which took longer than the first performance.

## Summary: 
After 6 total attempts, the first one from the 'AlphabetSoupCharity.ipynb' file was closest to the accuracy score. In the second file, 5 attempts were made to optimize the model performance, however did not achieve the target score and remained in the (.50 - 0.55) range. To solve this classification problem, I recommend utilizing a random forest model since both output and feature selection of random forest models are easy to interpret, and they can easily handle outliers and nonlinear data. 
