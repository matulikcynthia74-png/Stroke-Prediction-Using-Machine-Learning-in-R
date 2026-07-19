**Stroke Prediction Using Machine Learning in R**





**Overview**



Stroke is a leading cause of disability and death worldwide with LMICs accounting for three-quarters of all stroke cases. These are, however, deaths and complications that are preventable with early detection. Data Science methods such as Machine Learning predictive modelling and classification techniques including logistic regression, Gradient Boosting Trees, and Random Forest have stronger generalization and feature expression capabilities to learn and map complex nonlinear relationship between variables; and therefore, better at predicting high risk stroke patients.





\- Primary objective is to develop a predictive model for stroke.





\- Secondary objectives;



&#x20; - Compare the predictive performance of:

&#x20; 

&#x20;   - Logistic regression

&#x20;   

&#x20;   - Decision tree

&#x20;   

&#x20;   - Random forest

&#x20;   

&#x20;   - XGBOOST

&#x20;   

&#x20; - Select the best-performing model.

&#x20; 

&#x20; - Report the important predictors from that model.





**Dataset**



\- Source: https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset

\- Number of observations: 5110

\- Outcome: 	Stroke

&#x09;	No stroke

\- Predictors:	Age

&#x09;	Gender

&#x09;	BMI

&#x09;	Hypertension

&#x09;	Heart disease

&#x09;	Smoking status

&#x09;	Average glucose level

&#x09;	Residence

&#x09;	Work type

&#x09;	Marital status





**Methods**



Importing raw data to R

&#x20;     ↓

Data cleaning (completeness, consistency, and duplicates)

&#x20;     ↓

Descriptive statistics (Test for variable association with the outcome)

&#x20;     ↓

Feature engineering (bmi imputation, etc)

&#x20;     ↓

Class imbalance correction (Upsampling)

&#x20;     ↓

Model development (Logistic, Decision Tree, Random Forest, XGBOOST)

&#x20;     ↓

Hyperparameter tuning using 10 fold cross-validation (Decision Tree, Random Forest, XGBOOST)

&#x20;     ↓

Performance evaluation

&#x20;     ↓

Feature importance





The models were evaluated based on the following metrics; Area Under the Curve (AUC)/model discrimination, Precision-Recall AUC, Balanced accuracy, Sensitivity, Specificity, Precision, and F1-Score.







**Results**



&#x20; - XGBOOST model demonstrated the best overall predictive performance, achieving the highest ROC AUC (0.742) with a sensitivity of 0.708. The model also recorded the highest Precision-Recall AUC (0.205).

&#x20; 

&#x20; 

&#x20; - Logistic Regression model showed competitive performance with an AUC value of 0.733 and attaining the highest sensitivity of 0.736. Although the XGBOOST model is better at discriminating between individuals with stroke and those without stroke, the logistic regression model captured more individuals with stroke compared to XGBOOST.

&#x20; 

&#x20; 

&#x20; - The decision tree had the lowest AUC (0.706), however, it recorded the highest sensitivity (0.736) as the logistic regression model. Further, the decision tree has higher precision, balanced accuracy, F1-score compared to every other model. 

&#x20; 

&#x20; 

\- Generally, the best performing model was XGBOOST, followed by Decision Tree, Logistic Regression, and finally Random Forest.





\- While the models were able to identify a good percentage of stroke cases, the precision was fairly low accounting for the very low number of stroke cases (high class imbalance).





**Feature Importance**



The top predictors of stroke using the XGBOOST model were:

1. Elderly age group (>=65 years).
2. Middle-aged group (45-65 years)
3. Average glucose level (Diabetic (>=137mg/dL))
4. Heart disease
5. Hypertension.





Cynthia Matuli Stroke Prediction Project.

