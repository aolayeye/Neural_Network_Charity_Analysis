# Neural_Network_Charity_Analysis
## Overview
Alphabet Soup is a non-profit organization
In this project we will implement a neural network binary classifier that is capable of predicting whether applicants for donations will be successful if funded by Alphabet Soup. We will prepare input data, design, train, evaluate, and export neural networks to use in any scenario.
## Results
##### Data Processing
1. Feature List

![Feature_List](https://user-images.githubusercontent.com/67847583/131268029-882652b3-4531-4262-831e-e6ad5b908828.png)
2. Columns to be dropped.

The EIN and the Name column are non-beneficial to the model thus we remove them. Similarly, the STATUS column contains more than 98% the same value; the inclusion or exclusion of this column does not improve or decrease model performance
STATUS
![Status_Column](https://user-images.githubusercontent.com/67847583/131268084-58826bc2-fa5d-4c69-8171-9e4bbb9fc9a8.png)

##### Compiling, Training, and Evaluation
