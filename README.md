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

#### Attempt 2: Creating more bins for rare occurrences of categorical variable
A second attempt at improving model performance was creating more bins for the APPLICATION_TYPE and CLASSIFICATION columns. This attempt had no impact by themseleves on model performance.

#### Attempt 3: Incarease number of neurons
A third attempt at improving performance was increasing the number of neurons in the hidden layer. This attempt did not increase model accuracy

#### Attempt 4: Incrase number of hidden layer and changing activation functions
A fourth attempt included incrasing number of hidden layers and changing activation functions. Individually, these attempts did not raise model accuracy beyond 72%
