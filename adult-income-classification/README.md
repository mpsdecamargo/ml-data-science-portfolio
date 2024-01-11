# INTRODUCTION
This is a small project based on binary classification on an imbalanced dataset. I decided to do it in order to learn and practice my skills by following a tutorial and complementing it based on new methods I learned(Hyperparameter Tuning and Cross-Validation).

Note: I know the level of steps taken, such as the Hyperparameter Tuning steps may be overkill for this small dataset, but my purpose was to practice for my next projects.

# PROBLEM DEFINITION
In this machine learning portfolio project, the focus is on predicting adult income levels based on various demographic and employment-related features. The project involves addressing challenges related to data cleaning and handling imbalanced datasets to build a robust income prediction model.

The primary goal of the Adult Income Prediction project is to develop a machine learning model capable of predicting whether an adult's income exceeds a certain threshold, given a set of features such as age, education, occupation, and more. The prediction of income levels is essential for understanding socioeconomic factors and tailoring public policies accordingly.

# ABOUT THE DATASET
In this project, we will use a standard imbalanced machine learning dataset referred to as the “Adult Income” or simply the “adult” dataset.

The dataset is credited to Ronny Kohavi and Barry Becker and was drawn from the 1994 United States Census Bureau data and involves using personal details such as education level to predict whether an individual will earn more or less than $50,000 per year.

The Adult dataset is from the Census Bureau and the task is to predict whether a given adult makes more than $50,000 a year based attributes such as education, hours of work per week, etc..

— Scaling Up The Accuracy Of Naive-bayes Classifiers: A Decision-tree Hybrid, 1996.

The dataset provides 14 input variables that are a mixture of categorical, ordinal, and numerical data types. The complete list of variables is as follows:

Age, Workclass, Final Weight, Education, Education Number of Years, Marital-status, Occupation, Relationship, Race, Sex, Capital-gain, Capital-loss, Hours-per-week, Native-country.

The dataset contains missing values that are marked with a question mark character (?).

There are a total of 48,842 rows of data, and 3,620 with missing values, leaving 45,222 complete rows.

There are two class values ‘>50K‘ and ‘<=50K‘, meaning it is a binary classification task. The classes are imbalanced, with a skew toward the ‘<=50K‘ class label.

‘>50K’: majority class, approximately 25%. ‘<=50K’: minority class, approximately 75%. Given that the class imbalance is not severe and that both class labels are equally important, it is common to use classification accuracy or classification error to report model performance on this dataset.

[Source](https://machinelearningmastery.com/imbalanced-classification-with-the-adult-income-dataset)

# CONCLUSION

Considering F1 Score, the best model is XGBoost, with overall 86.32% accuracy, 72.73% F1 Score and Training Time 33.69 seconds for 10 cross-validation runs.

Considering overall accuracy, LGBM (87.38% accuracy, 71.11% F1 Score) is the best because it took so much less time to run and with an incredible performance. It's better performance with 1.5% the training time of the GBM model.

In conclusion, F1 Score is a more appropriate choice of evaluation with imbalanced datasets, but this assessment considered cross-validation in the final results.
