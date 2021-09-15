1. Variance Threshold Feature Selection
    Feature with a higher variance means that the value within that feature varies or has a high cardinality. On the other hand, lower variance means the value within the feature is similar, and zero variance means you have a feature with the same value.

2. Univariate Selection using SelectKBest
    - combining the univariate statistical test (chi2, Pearson-correlation) with selecting the K-number of features based on the statistical result between the X and y.
3. Recursive Feature Elimination or RFE
    This method only works if the model has coef_ or features_importances_ attribute
4. SelectFromModel
    SelectFromModel feature selection is based on the importance attribute (often is coef_ or feature_importances_ but it could be any callable) threshold. By default, the threshold is the mean.
5. Sequential Feature Selection or SFS
    SFS-Forward made a feature selection by starting with zero feature and find the one feature that maximizes a cross-validated score when a machine learning model is trained on this single feature. Once that first feature is selected, the procedure is repeated by adding a new feature to selected features. The procedure is stopped when we find the desired number of features is reached.
    SFS-Backward follows the same idea but works in the opposite direction: It starts with all the features and greedily removes all the features until it reached the desired number of features.

https://towardsdatascience.com/5-feature-selection-method-from-scikit-learn-you-should-know-ed4d116e4172