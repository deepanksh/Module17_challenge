# Module17_challenge
Credit_Risk_Analysis
Overview of the analysis:
Credit risk is very tough to predict. In this project we want to take a look at how all the factors in our loan_stats csv help predict whether someone is low or high risk status. One method that data scientists use for this type of issue is creating a model and then evaluate and train the models that they create. In this specific project we are using imbalanced-learn and scikit-learn libraries to build models and evalute them using a resampling method. In the first couple of models I oversampled the data using randomoversampler and smote algorithms and undersample the data with the clustercentroid algorithm. In the remaining models I used a combination approach to over and undersample the data using smoteenn. Finally, I compared two machine learning models that minimize bias, balancedrandomforestclassifier and easyensembleclassifier.

Results:
Naive Random Oversampling results: Our balanced accuracy test it 67%, the precision for the high_risk has a very low positivity at 1% and the recall is 74%
naive

SMOTE oversampling results: the accuracy score is 66.2%, the precision for the high_risk loans has a low positvity again at 1% and recall is 69% overall
smote

Undersampling results: balanced accuracy score is 66.2% overall, the precision is at 99% and the recall is 41%
undersampling

Combination(over and undersampling) results: balanced accuracy score is 54.7% the precision is 99% and the recall is 57% overall
combination

Balanced Random Forest Classifier results: the accuracy score is 77.2% the precision is 99% and the recall is 88%
random forest

Easy Ensemble AdaBoost Classifier results: the accuracy score is 91.7% the precision is 99% and the recall is 94%
ensemble

Summary:
In the first four models we undersampled, oversampled and did a combination of both to try and determine which model is best at predicting which loans are the highest risk. The next two models we resampled the data using ensemble classifiers to try and predict which which loans are high or low risk. In our first four models our accuracy score is not as high as the ensemble classifiers and the recall in the oversampling/undersampling/mixed models is low as well. Typically in your models you want a good balance of recall and precision which is why I recommend the ensemble classifiers over the first four models. It appears that the Easy Ensemble had the best balance of all the models because of it's high accuracy score and good balance of precision and recall scores.