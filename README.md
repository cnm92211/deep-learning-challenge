# Deep-learning-challenge

# **Background**
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special considerations for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively


# Neural Network Model Report for Alphabet Soup Charity

## Overview of the Analysis

The analysis aims to leverage machine learning to help Alphabet Soup Charity make more informed decisions about which projects to fund. A deep learning model was developed to predict the success of projects based on several features. The goal was to achieve a predictive accuracy higher than 75%.

## Results

### Data Preprocessing

- **Target Variable**: 
  - The target variable for the model is "IS_SUCCESSFUL," which is a binary variable indicating the success of the funded project.
  
- **Feature Variables**: 
  - The features for the model include 'APPLICATION_TYPE,' 'AFFILIATION,' 'CLASSIFICATION,' 'USE_CASE,' 'ORGANIZATION,' 'STATUS,' 'INCOME_AMT,' and 'SPECIAL_CONSIDERATIONS.'
  
- **Variables Removed**: 
  - 'EIN', 'NAME' were removed as they are identification variables and not useful for the model.

### Compiling, Training, and Evaluating the Model

- **AlphabetSoupCharity Model**: 
  - **Neurons and Layers**: Two hidden layers with 80 and 30 neurons. 
  - **Activation Functions**: Used ReLU for hidden layers and Sigmoid for the output layer.
  - **Performance**: 
    - Loss: 0.5542
    - Accuracy: 72.3%

- **Charity_Optimization_1 Model**: 
  - Drop additional non-beneficial ID columns, 'EIN', 'NAME', and 'ORGANIZATION'
  - **Performance**: 
    - Loss: 0.5605
    - Accuracy: 72.34%

- **Charity_Optimization_2 Model**: 
  - Adjusted the number of layers for further optimization.
  - **Performance**: 
    - Loss: 0.5623
    - Accuracy: 72.2%

- **Charity_Optimization_3 Model**: 
  - Added a third hidden layer and used different activation functions.
  - **Performance**: 
    - Loss: 0.5623
    - Accuracy: 72.3%

- **Achievement of Target Model Performance**: 
  - No, the models did not achieve the target performance of 75% accuracy.
  
- **Steps for Increasing Performance**: 
  - Adjusted the number of epochs.
  - Introduced an additional hidden layer.
  - Experimented with different activation functions.

## Summary

- The deep learning models, despite various optimization strategies, were unable to achieve the target performance of 75% accuracy. The accuracy hovered around 72-73%.
  
- **Recommendation**: Given that the neural network models were unable to reach the desired performance, it may be beneficial to try ensemble methods like Random Forest or Gradient Boosting for this classification problem. These models are effective for binary classification problems and may capture the feature importance more effectively.

This report captures the efforts made in building and optimizing the deep learning model for Alphabet Soup Charity's funding decisions.