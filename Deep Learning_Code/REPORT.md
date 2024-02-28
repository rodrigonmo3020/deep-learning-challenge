# Module 21 Report

## Overview of the Analysis
*   This code is made to read and clean a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures, so this code is made also to train and evaluate a model based on the result of the given found. 

*   The dataset displays information like Organization type, Income classification, Funding amount requested and Affiliated sector of industry, which are the most representative information for the analysis

*   The variable that was aimed to predict was the IS_SUCCESSFUL that states if the money was used effectively or not.

*   We went through bellow machine learning process as part of this analysis:
    * 1- Read and display the data
    * 2- Clean the data in order to get rid of non relevant infromation.
    * 3- Bining the variables that contain a small number of data points in order to get categorical variables together on a single variable.     
    * 4- Split the data into training a testing datasets using the function train_test_split
    * 5- Create a neural network model by assigning the number of input features and nodes for each layer using TensorFlow and Keras to create a binary classification model that can predict if an Alphabet Soup-funded organization will be successful based on the features in the dataset.
    * 6- Compile and train the model.
    * 7- Evaluate the model’s performance by generating an accuracy score.

## Results
* Data Processing
    * Variable target of the model: IS_SUCCESSFUL
    * Features of the model: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT.
    * Variables removed because they are neither targets nor features: EIN, NAME

* Compiling, Training, and Evaluating the Model
    * 1st model attempt:
        layers:  2
        neurons: 110
        activation function: 'relu'
        epochs: 100
        model performance: 0.725 (accuracy)

    * 2nd model attempt:
        layers:  3
        neurons: 300
        activation function: 'tanh'
        epochs: 100
        model performance: 0.723 (accuracy)

    * 3rd model attempt:
        layers:  3
        neurons: 430
        activation function: 'relu'
        epochs: 100
        model performance: 0.727 (accuracy)

## Summary
*   The accuracy target assigned for this model was for 75%, however the average results of the deep learning model was of 72%. This accuracy result reveal the limitation of the data to predict if the given found by the Alphabet Soup foundation will result on a successful outcome conssidering the current variables. As a recomendation, a tree-based model can be use on this dataset for a better prediction since it looks more like a non-linear relationship data problem. A tree-based model can be trained on a small piece of the original data and create a decision tree thatat the same time can be combined in small decision trees to create a strong classifier and also can be efficently on large datasets.*
