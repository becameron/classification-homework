# Classification Homework: Risky Business
## Description

The following assignment evaluates different methods of classification when faced with imbalanced data. Using the Lending Club Loans Data, each classification model will predict an individual's loan status as 'high risk' or 'low risk' using the following features:

* Loan Size
* Interest Rate
* Homeownership Status
* Income
* Debt to Income
* Number of Accounts
* Derogatory Marks
* Total Debt

Each classification model will be evalated on the basis of balanced accuracy score, recall, and geometric mean. The following algorithms will be used:

**Resampling**
* Naive Random Oversampler (Oversampling)
* SMOTE (Oversampling)
* Cluster Centroids (Undersampling)
* SMOTEENN (Combination)

**Ensemble Learning**
* Balanced Random Forest Classifier
* Easy Ensemble Classifier

----

### Data Cleaning

* The target (loan status) was removed from the dataframe and assigned to the variable 'y'.
* The remaining features were transformed in the following way:
    * The feature 'homeowner' reflected categorical, qualitative data (mortgage, rent, own) as such the feature was transformed into dummy variables using the function np.get_dummies() for input into the model. 
    * The homeowner dummy variables were removed from the dataframe. The remainder of the quantitative data was scaled using the StandardScaler() function.
* The remaining features were then combined into a dataframe and assigned to the variable 'X'.


------
## Summary of Findings

The ensemble methods of classification overall yielded the highest balanced accuracy scores, recall, and geometric means. Of the ensemble methods, the Easy Ensemble Classifier had the highest balanced accuracy score.  