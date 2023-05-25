# Gold_Recovery_Prediction_Model

This code is a series of steps taken to predict the amount of gold recovered from gold ore.

# Data Preprocessing
The code then preprocesses the loaded data by:

* Dropping any rows with missing target values.
* Filling any remaining missing values with forward fill method.

# Exploratory Data Analysis (EDA)
The code performs exploratory data analysis, including:

* Checking the data info and displaying the first few rows.
* Comparing the columns of the training and testing datasets.
* Checking the shape of the datasets before and after merging.
* Computing and printing the Mean Absolute Error (MAE) between the actual and computed recovery.
* Plotting histograms to show the concentration of metals at different stages.
* Plotting KDE plots to show the feed size distributions of the training and testing datasets.
* Plotting the total concentrations of all substances at different stages.
* The code cleans the data by removing any zero values for concentrations in the training dataset and aligns the training and test datasets to have the same set of columns.

# Workflow

* **Model Training**
<br>The code uses three models for training: Decision Tree, Random Forest, and Linear Regression. Hyperparameters for the tree-based models are determined by grid search.

* **Model Evaluation**
<br>The code evaluates the models by cross-validation and calculates the sMAPE (Symmetric Mean Absolute Percentage Error) for each model. 
The best performing model is then selected and applied to the test set to evaluate its performance.

* **Test Evaluation**
<br>After model training and validation, the model's performance is evaluated on the test dataset. In this code, the trained Random Forest model is used to predict the target values on the test set, and the sMAPE (Symmetric Mean Absolute Percentage Error) score is calculated for these predictions.

* **Comparison with Dummy Model**
<br>To provide a benchmark for the trained model's performance, a dummy model is used to predict the target values on the test set. The dummy model simply predicts the mean of the target values in the training set. The sMAPE score is calculated for the dummy model's predictions, and this score is compared with the sMAPE score for the trained model's predictions. This comparison helps to evaluate how much better the trained model is than a simple baseline model.

# Dependencies
This code requires the following Python packages:

* pandas for data manipulation and analysis.
* numpy for numerical computations.
* matplotlib and seaborn for data visualization.
* sklearn for machine learning tasks.
* scipy for scientific computations.
* DummyRegressor for comparison with the dummy model 

# Conclusion
This code presents a comprehensive workflow for predicting gold recovery from ore. It includes data preprocessing, EDA, feature selection, model training, evaluation, and comparison with a dummy model. The systematic approach and insights gained contribute to improved gold recovery prediction models in the mining industry.
