# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### SAMNIT MEHANDIRATTA

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
Negative values: If the predictions contain negative values and the submission guidelines specify that only non-negative values are allowed, you may need to set the negative values to zero or a minimum allowed value.
Outliers: If the predictions contain extreme values that are significantly larger or smaller than the majority of the values, you may need to remove or replace these values to avoid skewing the results.
Incorrect format: If the predictions are not in the required format, you may need to reformat the predictions to meet the submission guidelines.


### What was the top ranked model that performed?
Best model: "WeightedEnsemble_L3"

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
You comvert the datetime to separate day, month, year by extracting values after converting the datatype of the column to datetime.

### How much better did your model preform after adding additional features and why do you think that is?
The model drastically outperformed it's previous version. This can be due to the fact that there were better features to learn on.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
Hyperparameter tuning allowed me to complete the model training in 60 seconds without compromising much on the Kaggle score.

### If you were given more time with this dataset, where do you think you would spend more time?
I would spend more time learning about the origin so as to better understand how I can derive meaning to this data by engineering the features and finding out newer and simpler meanings out of the various columns.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
model	hpo1	hpo2	hpo3	score
0	initial	1.79221	1.79221	1.79221	1.79221
1	add_features	0.64795	0.64795	0.64795	0.64795
2	hpo	0.66328	0.66328	0.66328	0.66328

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](https://github.com/lankabhedi/nd009t-c1-intro-to-ml-project-starter/blob/master/model_test_score.png)

## Summary
The initial model had a score of 1.79221, but the performance was improved by creating additional features and converting the datetime column into separate columns for day, month, and year. The best-performing model was the "WeightedEnsemble_L3" model, with a score of 0.64795. Hyperparameter tuning allowed the model to be trained in 60 seconds without significantly affecting the Kaggle score. If given more time with the dataset, the practitioner would spend more time learning about the origin of the data and engineering additional features to improve the model's performance. The model's training scores and Kaggle scores are shown in the provided line plots.
