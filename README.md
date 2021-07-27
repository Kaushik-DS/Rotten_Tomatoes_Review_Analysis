# Rotten_Tomatoes_Review_Analysis
Analyzed to to predict the sentiment class label of a review on the basis of the numerical features andImplemented three different classification algorithms namely Support Vector Machines, RandomForest and Logistic regression
# Model Tuning and comparisons:
Implemented three different classification algorithms namely Support Vector Machines, Random
Forest and logistic regression. We tuned each model by passing different hyper parameter values
and trained using k-fold cross validation with 2 k-folds and replications as 10 and plotted the
corresponding accuracies for each models with different hyper parameters passed.
# Model 1: SVM
<br > Support vector machines (SVM) are an effective family of supervised classifier for data
with complex non-linear structures.
<br >We use kernel trick to map original data into high dimensional spaces with less
computational cost.
<br >The performance of support vector machine classifiers can be sensitive to the choice of
kernel function and hyper parameters.
<br >Here we used Gaussian Radial Basis Function as kernel function which takes two
parameters Cost C and Sigma.
<br >Cost function is the penalty term used to controls training error and margins in the data,
Sigma is used to control over fitting and under fitting of the data that is it helps to
generalize the data well.
<br >We took different values for C and sigma and trained the SVM model with different
combination of values and plotted the validation accuracy across the different parameter
values using k-fold cross validation technique.
<br >The method here used is “svmRadial” which indicates SVM - GRBF model for train
function and data here used is train data and the target variable is class.
<br >trControl takes trainControl parameters which indicates k-fold cross validation and
tuneGrid takes values of the expanded grid value combinations of parameters C and
sigma.
 Optimal cost and sigma value obtained were sigma = 0.001 and C = 1.
# Model 2: Random Forest
<br >Random Forest is a powerful and flexible ensemble learning procedures, improves the
prediction performance of a classifiers.
<br >andom forests uses the same machinery of bagging, but a clever tweak that is at each
split of the tree use a random subset of the input variables which reduces the correlation
between trees and improves the predictive performance.
<br >Here the hyper parameter for random forest model is mtry which is number of predictors
for split.We took here different mtry values starting from 2 to 79 by increasing at each
step value as 5 and 79 which is the total number of parameters also included in the list.
<br >The method used here is ‘rf’ which indicates random forest model for the train function
and data we used here is train data and the target variable is “class”.
<br >trControl takes trainControl parameters which indicates k-fold cross validation and
tuneGrid takes values of the expanded grid value combinations of mtry parameters.
<br >Optimal value for mtry obtained from the models is mtry = 7
# Model 3: Logistsic Regression
<br >Logistic regression is one of the best model when the target variable is binary response
variable.
<br >Glmnet method that fits generalized linear and similar models via penalized maximum
likelihood. The regularization path is computed for the lasso or elastic net penalty at a
grid of values (on the log scale) for the regularization parameter lambda. The algorithm is
extremely fast and can exploit sparsity in the input data.
<br >Here it takes two parameters alpha and lambda, alpha =0 indicating Ridge Regression
which is a default value and alpha = 1 indicating Lasso Regression we took alpha =0 and
lambda being penalty coefficient takes different range of values.
<br >The method used here is ‘glmnet’ which indicates Logistic Regression model for the train
function and data we used here is train data and the target variable is “class”.
<br >trControl takes trainControl parameters which indicates k-fold cross validation and
tuneGrid takes values of the expanded grid value combinations of alpha and lambda
parameters.
<br >Optimal value for lambda obtained from the models were alpha = 0 and lambda = 0.175
