# deep-learning-challenge
### Overview of the analysis: 
For this analysis, Alphabet Soup would like a tool to help identify future applicant's success if they were to fund their ventures.  Therefore, with the dataset that was provided by Alphabet Soup, which includes over 34,000 organizations that they have funded over the years, I was able to preprocess the data and create a module to predict the success of future applicants.

### Results: 
* In the starter code notebook, I preprocessed the data, built the model and compiled, trained, and evaluated the model.  In the AlphabetSoupCharity_Optimization notebook, I used the same preprocessed data, and optimized the data using different optimization techniques to achieve an accuracy score over 75%.

#### Data Preprocessing

* What variable(s) are the target(s) for your model?
  * The variable that was used as the target for the model was the column of "IS_SUCCESSFUL".
* What variable(s) are the features for your model?
  * The variables used for the features in the model were the rest of the columns from the dataframe.
* What variable(s) should be removed from the input data because they are neither targets nor features?
  * I removed the columns, EIN and NAME, since they did not provide any data which would assist in predicting success of future applicants.

#### Compiling, Training, and Evaluating the Model

##### How many neurons, layers, and activation functions did you select for your neural network model, and why?
* In the original starter code notebook, I used 2 hidden layers, one layer containing 80 units, and the other layer containing 30 units. Both layers used relu as the activation function, and the output layer used one unit and the sigmoid activation function.  I also used 100 epochs to train the model.
##### Were you able to achieve the target model performance?
* I was not able to achieve the target model performance and the accuracy came down to .7293.

![Original Result](https://github.com/Lillyrue/deep-learning-challenge/blob/main/Screenshots/Screenshot%202024-02-27%20215948.png)

##### What steps did you take in your attempts to increase model performance?
* In the AlphabetSoupCharity_Optimization notebook, I optimized the model three times. In the first optimization, I increased the units in both layers, and gave an accuracy of .7290, which is a slight decrease from the original result.

![First Optimization Result](https://github.com/Lillyrue/deep-learning-challenge/blob/main/Screenshots/Screenshot%202024-02-27%20200918.png)
* In the second optimization, I decreased the units, and I changed the activation function in the first layer to tanh, which gave an accuracy of .7272.

![Second Optimization Result](https://github.com/Lillyrue/deep-learning-challenge/blob/main/Screenshots/Screenshot%202024-02-27%20200959.png) 
* In the last optimization, I increased the units in both layers, changed the activation function back to relu in the first layer, and increased the epochs to 150, which resulted in an accuracy of .7298, which is a slight increase from the original result.

![Last Optimization Result](https://github.com/Lillyrue/deep-learning-challenge/blob/main/Screenshots/Screenshot%202024-02-27%20201015.png)
### Summary: 
Overall the results of the deep learning model did not achieve over 75% in accuracy.  Some recommendations for this model might be to delete more columns in the dataframe to give a higher result or adding additional data that Alphabet Soup may have that may make a difference in predicting successful applicants. What seemed to increased the result in the last optimization was to increase the units and the epochs, and in combination of deleting some columns, might result in an accuracy of over 75%.
