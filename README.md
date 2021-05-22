# Credit_Card_Fraud_Detection

Data from the Kaggle link: https://www.kaggle.com/ananta/credit-card-data.

Joining all the tables with required columns and excluding the Customers without Card because we need transactions for further steps.
Used dataprep for EDA and understanding the data information. EDA was challenging because of class imbalance of target.
After analysis on the data set selected Categorical columns for preprocessing, created new columns with encoding, changed the required dataType and at last merged the processed columns to the original dataFrame.
On observing the data information and comaparison with 'Fraud_Flag' few columns were dropped.
The data was ready with all required Independent Columns then target & features were selected.
As the data column's values are of different scale then Scaling was performed on the it.
The train_test split was completed on the scaled data for training on the LogisticRegression with imbalanced data and result was biased to label '0'.
For balancing the data SMOTE(Synthetic Minority Oversampling Technique) technique is used , after using this the class was balanced and then train_test split was performed on new synthetic data.
For finding the best model LogisticRegression, XGBoostClassifier, RandomForest, DecisionTreeClassifier and SVC were used. These model were tuned with best parameters with the help of GridSearchCV .
Among all the models SVC performed better and with reduced overfitting results.
