# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Bhanvi Nayer

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
There were three prediction models that i submitted. First, the basic one with no hyperparameters and add features. Second, the model with some additional features. And third, the Autogluon model with hyperparameters. Before submiting it was neccesarry to ensure there were no negative prediction values.

### What was the top ranked model that performed?
The top ranked model that performed was new features with hyperparameters Tabular AutoGluon model having the best model as WeightedEnsemble_L3, with the kaggle score of 0.47640.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
The temperature categories exhibited a normal distribution. I thought of enhancing the model by splitting the datetime into year, month, day, and hour components as for the analysis it was not very easy to comprehend and overlapping. Seasonal and weather patterns were distinct. Workday and holiday fields are binary, while humidity and windspeed display non-uniform distributions.

### How much better did your model preform after adding additional features and why do you think that is?
The model performed much better after splitting of the datetime into years, months, day and hours. It brought kaggle score from 1.80364 to 0.61212 improving it by around 66.66%. This enhancement likely resulted from capturing more detailed temporal and categorical information, allowing the model to better understand and predict complex patterns in the dataset.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
The model improved alot after adding different hyperparameters. I referred to the AutoGluon Tabular Documentation for adding the hyperparameters for improving the model.

### If you were given more time with this dataset, where do you think you would spend more time?
If i were given more time, i'd like to experiment with the autogluon tabular model and try hyperparameters tuning with different parameters, models and change in values.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1: timelimit|hpo2: presets|hpo3: hp|score|
|--|--|--|--|--|
|initial|600|best_quality|given|1.80364|
|add_features|600|best_quality|given|0.61212|
|hpo|600|best_quality|Tabular AutoGluon|0.47640|


### Create a line plot showing the top model score for the three (or more) training runs during the project.



![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.



![model_test_score.png](img/model_test_score.png)

## Summary
AutoGluon was utilized extensively for automated model stacking and training on tabular data, significantly improving results through feature engineering and EDA. However, hyperparameter tuning with AutoGluon, while powerful, is time-consuming and requires careful configuration for optimal performance.

