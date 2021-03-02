# Health-Insurance-Cross-Sell-Prediction

### Introduction
A health insurance company intends to improve its revenue by cross selling vehicle insurance. To discover the potential value of this business, the corporate collected data including customers’ information and their responses to the new service. This project moves the evaluation of business into analysis level. It aims to conduct Exploratory Data Analysis, build several models, train them with existing data, and select the one with optimal performance. The model will detect healthcare members who are more likely to register for vehicle insurance, which could help company focus more on potential clients.

### Data
The data includes 381,109 rows and 12 columns. Most variables are categorical, and several predictors are regarded as dummy variables. Predictors (x variables) include *id, gender, age, driving license, region code, previously insured, vehicle age, vehicle damage, annual premium, policy sales channel, and vintage*. Output (y variables), *response*, refers to whether customers are interested in vehicle insurances. It shows significant imbalance between “0”, who are not interested, and “1”, who are interested. Most of the data are “0” and the remaining rows are “1”. 

### Methods: 
Describe characteristics of predictors with Exploratory Data Analysis. Compare information of customers who are interested in vehicle insurance to those who are not interested. Process data in three different methods to create three types of prepared data: data without any sampling, data with down sampling, data with SMOTE. Fit data into various machine learning models: lasso regression, ridge regression, decision tree, random forest, boosting, logistic. Assess outcome of each model.

### Results and Discussions:
The results show positive affect of SMOTE function on models’ performance since SMOTE function balanced data by creating more data with value “1” in y variables. Without SMOTE function, nearly all outputs are predicted as “0”. Though accuracy and specificity are high in this case, sensitivity is extremely low. SMOTE function traded off few accuracy and specificity rate to improve sensitivity and ROC curve. 

Among all sorts of pipelines, SMOTE along with Random Forest generates the most decent result. For this analysis, sensitivity is 95%, specificity is 70%, accuracy is 82%, and AUC value is 0.80, which outstrip other competing models. Top 5 features selected from Random Forest are: *vehicle damage, previously insured, age, annual premium, and policy sales channel*.
