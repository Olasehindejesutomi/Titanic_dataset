# Titanic_dataset
To predict whether a person Died or Survived
Titanic Survival Prediction
Project Overview
This project uses passenger information from the Titanic dataset to
train and compare machine learning classification models that predict
whether a passenger survived.
Objective
Predict the Survived target from selected passenger characteristics
and compare model performance before and after hyperparameter tuning.
Dataset
The notebook loads a CSV file from data/titanic.csv. It also includes
an alternative example using Seaborn's built-in Titanic dataset.

The features selected in the notebook are: - Pclass --- passenger
class - Sex --- encoded as a numeric value - Age - SibSp ---
siblings/spouses aboard - PaCh --- the column name used in this
notebook for parent/child count aboard - Fare

The target is Survived: - 0 = did not survive - 1 = survived

Make sure the CSV contains the feature column names expected by the
notebook. If your dataset uses Parch rather than PaCh, update the
notebook's feature list and prediction function to use the matching
column name consistently.
Tools and Libraries
- Python
- Pandas and NumPy
- Matplotlib
- Scikit-learn
- Seaborn (used for the optional built-in dataset example)
Workflow
1. Load and inspect the Titanic data.
2. Explore summary statistics, missing values, and survival counts.
3. Plot the distribution of the Survived target.
4. Select passenger features and separate them from the target.
5. Encode the Sex column numerically.
6. Split the data into training and testing sets using an 80/20 split
   and stratification.
7. Scale features for Logistic Regression.
8. Train and evaluate Logistic Regression, Decision Tree, and Random
   Forest classifiers.
9. Tune Decision Tree and Random Forest hyperparameters with
   GridSearchCV and five-fold cross-validation.
10. Evaluate tuned models on the test set.
11. Use the trained model to try a survival prediction for a passenger
    example.
Models
- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
The notebook also imports Support Vector Classifier (SVC), though the
documented workflow primarily trains the three models listed above.
Model Evaluation
The notebook uses: - Accuracy - Classification report (precision,
recall, and F1-score) - Confusion matrix tools are imported for
evaluation

Run the notebook to generate results for your local dataset and
environment.
How to Run
1. Clone or download this repository.
2. Install the required libraries:
   pip install pandas numpy matplotlib scikit-learn seaborn jupyter
3. Place titanic.csv in the data/ folder.
4. Open and run Titanic_dataset.ipynb in Jupyter Notebook or
   JupyterLab.
Project Status
Educational machine learning project for practicing exploratory data
analysis, feature preparation, classification, model comparison, and
hyperparameter tuning.
Disclaimer
This project is for educational purposes. Predictions are estimates from
a model and do not establish what would have happened to any individual
passenger.
