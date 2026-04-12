## Spaceship Titanic Prediction
This project involves building a machine learning model to predict which passengers were transported to an alternate dimension during the Spaceship Titanic's collision with a spacetime anomaly.

## Project Overview
The notebook performs a complete data science workflow, including data cleaning, exploratory data analysis, feature engineering, and model training using a LightGBM classifier.

## Key Features
Data Health Reporting: A custom function data_health is used to provide a summary of the dataset's rows, columns, missing values, and statistical summary.

Missing Value Handling: Missing values in critical columns like Age, HomePlanet, CryoSleep, and Destination are handled using median and mode imputation.

## Feature Engineering:

Categorical features like HomePlanet and Destination are converted into boolean flags (e.g., home_earth, dest_TRAPPIST).

Unnecessary columns such as Name and Cabin are dropped to streamline the model.

## Model Training: A LGBMClassifier is trained using hyperparameters optimized through a search process (likely Optuna, as indicated by the trial logs).

Cross-Validation: The model's performance is evaluated using StratifiedKFold cross-validation to ensure stability and accuracy.

## Dependencies
The following Python libraries are required to run the notebook:

pandas

matplotlib

seaborn

scikit-learn

lightgbm

optuna (for hyperparameter tuning)

## How to Use
Ensure the train.csv and test.csv files are in the expected directory.

Run the cells in order to process the data and train the model.

The final predictions are saved in a submission-ready format containing PassengerId and the predicted Transported status.
