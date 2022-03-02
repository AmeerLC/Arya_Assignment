# Arya_Assignment

# *After completion of the EDA certain conclusions that can be drawn from the dataset are:*

All the features of he dataset are continuous. <br />
The distribution of output variable is 60:40. <br />
The data is non normal and highly skewed. <br />
Dataset is of different scale, hence normalaisation has to be done. <br />
As the dataet is highly dimensional, top features has to be selected before proceeding to model building. <br />

# Splitting
The entire dataset was split into train and test in the ratio 4:1. The splitting was startified as there was slight imbalance in the output distribution.\

# Feature Selection
Anova F score was taken to identify the best features as the input variables were continuous and the output variable was binary. There were 23 features that had F score more than the average f scores of all the features. Hence top 25 best features were selected for further steps.\

# Feature Scaling 
As the dataset was non- normal, min max scaler was used to scale the dataset before feeding it to the model for better performance.\

# Model Selection

* Naive bayes model - Multinomial NB model was used as the dataset was sparese and was capable of hantling large features. The model had good auc score but the accuracy and F1 score was comparitively low. There was no overfitting.
* KNN - The model performance was not satisfactory even after selecting the optimal k value
* Decision tree - The model was not overfitting. But the accuracy and auc score were low compared to other models.
* Random forest - The model had relatively high auc score and log loss. But the F1 score was low for the model. But this was one of the top 3 performing model.
* Logistic Regression - It was penalised with Ridge regression. The model was slighly overfitting in terms of F! score. But performance was comparitively better
* XG Boost - This model was the best performing model of all. But the difference between log loss of train dataset and test dataset slightly high
* Multi layered perceptron - The performance was not satisfactory. It was overfitting.

As the top 3 performing models were Random forest, Decision Tree and XG Boost, these 3 models were taken for soft voting and was tried on train and validation dataset. The result outperformed all the model in terms of log loss, auc score, f1 score and accuracy. Hence this model is selected as the final model to predict on est dataset.

