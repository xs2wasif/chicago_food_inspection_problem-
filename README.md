# Assignment - CHICAGO FOOD INSPECTION PREDICTION & OPTIMIZATION

## inspection_problem.docx 
Problem statement mentioning the details of the problem to solve. Thanks to Sustainabilist link which provides me support to prepare model training data. Already processed data is placed in "input" folder. 

https://www.sustainabilist.com/blog/chicago-data-analysis-a-internship-project
https://github.com/Sustainabilist/ChicagoDataAnalysis

# 1. Exploratory Data Analysis

## i. CFIP_solution_notebook_EDA.ipynb
This file contains very basic EDA. Thanks to the shared links in the problem statement. I havn't focused on EDA in solving the problem. However, I believe we can derive business level KPIs for performance management in the domain of Operational and financial reporting

Keeping the optimization as the ultimate goal, I have divided the problem into two categories:

1. Multi-class (High, Medium, Low) classification problem
2. Binary (Profitable visit (High, Medium) & Non-profitable visit (Low)) classification problem

# 2. Predicting the risk of restaurants commiting violations

## Components of modeling and prediction

1. Data standardization
2. Train/test/validation split (Generally, 80% training, 20% testing)
3. Feature Engineering (RFE/SelectK/Tree-based)
5. Class Imbalance (SMOTE)
6. Hyperparameter tuning (used Hyperopt. Tried GridSearch & RandomSearch but they were taking a lot of time for optimization. Played a little with Bayes Opt as well)
7. Classification Models 
    i. XGBoost
    ii. LightGBM
    iii. Random Forest
    iv. SVM (for binary setting)
    v. Neural Networks

Following notebooks contain various variations of above components to check the best combination providing the highest evaluation metrics. All the details of combination are added in "elm_summary_&_optimized_solution.xlxs".

### 1. Multi-class (High, Medium, Low) classification problem
#### CFIP_solution_notebook_MultiClass.ipynb
#### CFIP_solution_notebook_NN_MultiClass.ipynb 
##### CFIP_solution_notebook_NN_layer_parameter_search.ipynb
I tried to optimize nunmber of layers and node per layer on the dataset. However, due to resource limitation, the code breaks and provide no result. Though I run the code on a sample of dataset

### 2. Binary (Profitable visit (High, Medium) & Non-profitable visit (Low)) classification problem
#### CFIP_solution_notebook_BinaryClass

# 3. Optimizing :: minimizing number of visits for inspection & maximize operational profits

### elm_assignment_summary_&_optimizated_solution
This file contain summary of all the component combination used for prediction and what optimization each combination brings. I tried to be as thorough as possible while predicting to make the best optimization. This sheet contains summary considering the test-split as "unknown" label data to see what optimization is possible. Also it contains the most optimized based on the working. I would like to request to discuss this sheet so that I can explain the working done for optimization.

### elm_assignment_optimization_mechanics
This sheet explains optimization details and numbers which are present in "elm_assignment_optimization_mechanics". This present a detailed working of cost/profit working based on best, worst and optimized scenarios.

### Additional work
Please consider this an auxillary work aside from main optimization. The reason to present is to show-case working and method which can help us optimizaed further if we have additional information and some assumptions. 

1. Lagrange Optimization
2. Linear Programming (Production line problem) for resource optimization

I also thought to handle the problem using Dynamic programming (Knapsack) problem if we want to make all available inspectors profitable however the design of the problem only support greedy approches. We can use this appraoch if certain const or distances are included in the problem statement.

Looking forward to present demo on the working.

Adios.!

