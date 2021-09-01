# Neural_Network_Charity_Analysis
## Overview
Alphabet Soup is a non-profit organization
In this project we will implement a neural network binary classifier that is capable of predicting whether applicants for donations will be successful if funded by Alphabet Soup. We will prepare input data, design, train, evaluate, and export neural networks to use in any scenario.
## Results
### Data Processing
1. Feature List

![Feature_List](https://user-images.githubusercontent.com/67847583/131268029-882652b3-4531-4262-831e-e6ad5b908828.png)

2. Columns to be dropped.

The EIN and the Name column are non-beneficial to the model thus we remove them. Similarly, the STATUS column contains more than 98% the same value; the inclusion or exclusion of this column does not improve or decrease model performance
STATUS

![Status_Column](https://user-images.githubusercontent.com/67847583/131268084-58826bc2-fa5d-4c69-8171-9e4bbb9fc9a8.png)

### Compiling, Training, and Evaluation
To optimize the model, we used three hidden layers, with 90, 50, and 25 neurons for layer1, layer2, and layer3 respectively
#### Attempt 1: Dropping more columns
To increase model performance, we started by dropping more columns. Any columns dropped beyond the NAME, EIN, and STATUS colums either reduced model performance or did not increase model performance or did.

Model Accuarcy after dropping more columns

![Model_Accuracy_Drop_Columns](https://user-images.githubusercontent.com/67847583/131287022-99649371-a46f-4d4c-88bd-e0a375cbffc0.png)

#### Attempt 2: Creating more bins for rare occurrences of categorical variable
A second attempt at improving model performance was creating more bins for the APPLICATION_TYPE and CLASSIFICATION columns. This attempt had no impact by themseleves on model performance.

Model Accuracy after binning rare categorical occurences

![Model_Accuracy_Binning](https://user-images.githubusercontent.com/67847583/131287466-2cdfeaf8-0b40-4e86-9e25-a20ab569e024.png)


#### Attempt 3: Incarease number of neurons
A third attempt at improving performance was increasing the number of neurons in the hidden layer. This attempt did not increase model accuracy

Model Accuracy after increasing number of neurons

![Model_Accuracy_Increase_Neurons](https://user-images.githubusercontent.com/67847583/131288973-8ffdb72e-b10d-4805-867d-8ba919da4d59.png)

#### Attempt 4: Incrase number of hidden layer and changing activation functions
A fourth attempt included incrasing number of hidden layers and changing activation functions. Individually, these attempts did not raise model accuracy beyond 72%

Model Peformance after increasing number of hidden layers

![Model_Accuracy_Add_Hidden_Layers](https://user-images.githubusercontent.com/67847583/131287072-8500b839-2fad-4b51-a49a-0eec36981cfb.png)

#### Attempt 5: Using a different model: Random Forest
Random forests or random decision forests are an ensemble learning method for classification, regression and other tasks that operates by constructing a multitude of decision trees at training time. For classification tasks, the output of the random forest is the class selected by most trees.

With Random Forests, we can compute feature importance which can be used to determine the most important features. We can then focus on these features to determine if the our model accuracy improves.
After multiple tries with different feature combinations, we are able to determine that the CLASSIFICATION feature is a particularly noisy column. Also, the ASK_AMT column contains alot of outliers. Removing some the outliers together with some CLASSIFICATION records improved model performance to 75%

![AlphabetSoupCharityOptimization_RandomForest_ModelAccuracy](https://user-images.githubusercontent.com/67847583/131611487-e09807b2-506c-4bd2-a67c-873accb15ab2.png)

### Summary
While the neural network model may be a powerful machine learning algorithm, it did not do a good job at classifying which applicants requests for donation will be successful given the dataset we have.
Some of the steps to improve model accuracy may include:
1. One recommendation is to use a larger dataset to train the neural network model to learn the general distribution of the dataset without overfitting.
2. We may use the Balanced Random Forest Classifier which combines the decision of multiple trees to create a strong model accuracy

While model accuracy reached 75%, we may have a model that is overfiiting. That is why a larger dataset will be appropariate to train our neural network model or any other model we choose to use.
   

