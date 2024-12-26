This is a project done based on Kaggle's Loan Approval Prediction Series (https://www.kaggle.com/competitions/playground-series-s4e10/overview).

This series had 3 datasets: "train.csv", "test.csv", and the original dataset (https://www.kaggle.com/datasets/chilledwanker/loan-approval-prediction).

This project aims to do the following steps:
1. Create 3 versions of training data
   i. Using just "train.csv".
   ii. Using "train.csv" + original, where missing values are dropped.
   iii. Using  "train.csv" + original, where missing values are imputed.
2. Perform hyperparameter tuning on these 3 training sets for LGBM and XGB models.
   3 best models for each type of model was generated.
3. Try some aggregation of the models to find the best result:
   i. Stack: Simply taking the mean of the prediction of combined models.
   ii. Logistic Regression: Train a Logistic Regression using the predictions as data and ground truth as target.
   iii. Weighted Sum Optimization: Similarly treating predictions as data and ground truth as target, train the weights of the sum.
4. The best result was uploaded and was given a private score of 0.96242.

Description of the Files:
1. "data" files: Includes all the data needed to run the iPython Notebook. Also includes all data generated while running code.
2. "lgbm_model", "xgb_model": Located within data file. Stores the best models trained on LGBM and XGB using the dataset.
3. "lap_edapreprocessing.ipynb": Describes the process of exploratory data analysis and feature preprocessing done on the dataset.
4. "lap_lgbm_models.ipynb", "lap_xgb_models.ipynb": Includes the hyperparameter tuning process of the LGBM and XGB models respectively.
5. "lap_aggregation.ipynb": Includes the exploration on aggregation methods using the best models that were found in prior.

Please change each "path" variable in each notebook to the directory of your "data" file if you would like to run this code.
