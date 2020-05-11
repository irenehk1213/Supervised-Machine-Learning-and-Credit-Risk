# Supervised-Machine-Learning-and-Credit-Risk

Credit risk is an inherently unbalanced classification problem, as the number of good loans easily outnumber the number of risky loans. Thus, I need to employ different techniques to train and evaluate models with unbalanced classes, using imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling in this case. 

After running four different techniques: 

## 1) Oversampling (Naive Random Oversampling, SMOTE Oversampling) 
The idea is simple and intuitive: If one class has too few instances in the training set, we choose more instances from that class for training until it’s larger.
## 2) Undersampling 
Undersampling takes the opposite approach of oversampling. Instead of increasing the number of the minority class, the size of the majority class is decreased.
## 3) Combination (Over and Under) Sampling, SMOTEENN
SMOTEENN combines the SMOTE and Edited Nearest Neighbors (ENN) algorithms. SMOTEENN is a two-step process:

1. Oversample the minority class with SMOTE.
2. Clean the resulting data with an undersampling strategy. If the two nearest neighbors of a data point belong to two different classes, that data point is dropped.
## 4) Ensemble Learners
BalancedRandomForestClassifier and EasyEnsembleClassifier, both from imblearn.ensemble.

## Conclusion 
To begin with the conclusion, the results explain that there're none of the best models and I do not recommend any particular model; the models performance is evaluated based on the 1) precision 2)recall scores, and 3)the balanced accuracy score basically. When the test was previously evaluated in a study, the results were collated into the following table, called a confusion matrix. Precision = TP/(TP + FP); Sensitivity = TP/(TP + FN); And as you can see the result of the following imbalanced classification report at the end of the each model, none of them have overall balanced/ high enough result of precision, recall, and balanced accuracy score. Either or at least one output among them are insufficient to prove that they are performing outstanding. 
