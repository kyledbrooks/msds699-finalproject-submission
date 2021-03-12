# msds699-finalproject-submission

## Research Question: Can we predict whether an individual is going to die of heart failure given at-risk patient data?

In this repository, I explore creating a model on a Kaggle data set entitled "Heart Failure Prediction" (https://www.kaggle.com/andrewmvd/heart-failure-clinical-data). I preform preprocessing on the data to convert it into a format suitable for machine learning, and explore three different algorithms (Logistic Regression, Random Forest Classifier, and K-nearest neighbors). 

I utilize RandomSearchCV() and choose my metric to be `fbeta_score` to place more emphasis on recall, given that the scope of the prediction deals with human lives. I found that the ideal algorithm for the data was a `RandomForestClassifier()`. Additionally, I indentified the most significant features as age, ejection_fraction, and serum_creatinine. 

The model was tested via the testing set, and it seems that the model performs better on class 0 (patient is censored) than class 1 (patient dies). This is unfortunate as I would prefer to have better performance on class 1. For future work, I will create a model based on strictly the numeric features to see if that improves performance.