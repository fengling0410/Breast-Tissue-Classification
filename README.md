# Breast Tissue Classification with Machine Learning

### Background
Breast cancer is one the leading cancers among other cancers in the United States. This observation emphasizes the need for investigation in cancer detection and treatment. Early detection of Breast Cancer can guide physicians to take appropriate actions to prevent the spread of malignant cells to other parts of the body, which may cause a more complicated problem. Therefore, those patients identified in the initial stage of breast cancer have a higher survival rate. The use of machine learning in the medical fields can offer great insights to medical practitioners in the process of prediction and early diagnosis of breast cancer and yield better medical outcomes.

In this project, we built a classification model to predict the diagnosis of breast tissue based on tissue features such as radius, smoothness, compactness, and so on (8 predictors in total). This predictive model could be used to identify malignant tissues and speedup the diagnosis process for doctors and patients. The [Breast Cancer Wisconsin (Diagnostic) Data Set](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data/code) can be downloaded from Kaggle.

### Methods
We first performed PCA to visualize our dataset and to make our models more robust. Then, we built several classifiers to predict the diagnosis of breast tissue based on tissue features: Logistic Regression, GAM, Tree methods (Decision Tree and Random Forest), SVM, and Gradient Boosting. 

For hyper-parameters, we performed a grid search to try a set of hyper-parameter combinations, then chose the one with best performance. For a given hyper-parameter combination, we might use cross validation to tune model parameters when needed. For model evaluation, we constructed confusion matrices and compared statistics such as accuracy, specificity and sensitivity, which could give us an overall insight of model performance. 

### Results
The overall result is presented in the following Table:


