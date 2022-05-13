# Breast Tissue Classification with Machine Learning

### Background
Breast cancer is one the leading cancers among other cancers in the United States. This observation emphasizes the need for investigation in cancer detection and treatment. Early detection of Breast Cancer can guide physicians to take appropriate actions to prevent the spread of malignant cells to other parts of the body, which may cause a more complicated problem. Therefore, those patients identified in the initial stage of breast cancer have a higher survival rate. The use of machine learning in the medical fields can offer great insights to medical practitioners in the process of prediction and early diagnosis of breast cancer and yield better medical outcomes.

In this project, we built a classification model to predict the diagnosis of breast tissue based on tissue features such as radius, smoothness, compactness, and so on (8 predictors in total). This predictive model could be used to identify malignant tissues and speedup the diagnosis process for doctors and patients. The [Breast Cancer Wisconsin (Diagnostic) Data Set](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data/code) can be downloaded from Kaggle.

### Methods
We first performed PCA to visualize our dataset and to make our models more robust. Then, we built several classifiers to predict the diagnosis of breast tissue based on tissue features: Logistic Regression, GAM, Tree methods (Decision Tree and Random Forest), SVM, and Gradient Boosting. 

For hyper-parameters, we performed a grid search to try a set of hyper-parameter combinations, then chose the one with best performance. For a given hyper-parameter combination, we might use cross validation to tune model parameters when needed. For model evaluation, we constructed confusion matrices and compared statistics such as accuracy, specificity and sensitivity, which could give us an overall insight of model performance. 

### Results and Discussion
The overall result is presented in the following Table:
![alt text](https://github.com/fengling0410/Breast-Tissue-Classification/blob/main/result.png)

In this project, we have fitted Logistic Regression with regularization, Generalized Additive Model, Support Vector Machine, Decision Tree, Random Forest, Gradient Boosting Classifier, Adaboost and XGBoost. Among these models, Logistic Regression, GAM, SVM and Adaboost have the highest test accuracy and test AUC. The Logistic Regression model is comparatively simple and easy to understand, but with regularization it loses interpretability. GAM is easy to interpret, but it has high computation complexity. SVM has poor interpretability. Adaboost has high flexibility via ensemble learning and provides variable importance. 

Since in medical fields, doctors and researchers want decisions more than predictions, here we recommend using the Adaboost model to help explain and predict breast tumor category based on 30 tutor features. The model has the highest test accuracy and very high test AUC, and also provides insights about feature importance: texture_worst, concave points_worst and area_worst are the top three most important features. We hope that our project could provide insights for future tumor classification tasks and ease future research in this field.
