# CPSC392_Assignment2

Variable Descriptions:
age: age in years of person.
had_cancer: 0 if the person has NOT had cancer or has cancer, 1 if they have.
gender_id: Male, Female, Non-Binary, or Survey Choices Do Not Accurately Reflect My Identity.
income_in_k: income in thousands of dollars.
state: state person lives in.
credit_score: credit score.
num_credit_sources: number of sources of credit (includes credit cards, loans, car payments...etc).
utilization_rate: the % of a person's total credit they use on average each month. For example if you have 10,000 dollars in available credit, and use 2,000 your utilization rate would be 0.2 (20%).
gave_loan: whether or not the person got a loan.
Instructions
Build a KNN, Decision Tree, AND Logistic Regression model to predict whether or not someone got a loan using all the other variables.
If a variable/predictor has more than 2 categories, use get_dummies() to convert them into dummy variables (don't forget to remove the original column when training! see here).
use the train_test_split() to do an 80/20 split (make sure to use the SAME split when training all 3 models, do not re-split your data. We want each model to be trained on the same training set).
Appropriately z-score your continuous variables only (interval data like age...etc can be counted as continuous)
For KNN, include only continuous/interval columns as predictors. For Decision Tree and Logistic Regression use ALL columns (other than gave_loan).
For KNN, choose K by using GridSearchCV.
For Decision Trees, use GridSearchCV to choose max_depth, and make sure to check for overfitting.
Record the Train/Test accuracies, and print out confusion matrices for both train and test.
Evaluate Your Models (WRITE YOUR ANSWER IN MARKDOWN CELL)
A) Using accuracy AND confusion matrices, thoroughly discuss which model did best (if you had to pick one), how can you tell?
B) Are there differences in how accurate each of the three models you made in part 1 are for different gender IDs? (do NOT build a new model for this question. This is simply asking whether any of our models are more accurate when applied to different gender groups, regardless of whether gender was used in the model. If it helps, imagine you're about to deploy this model in the real world, and your boss asks whether the model is biased against/for certain gender groups).
C) Are your models better at predicting people who got loans, or didn't get loans? How can you tell? Discuss thoroughly the possible implications of this.
