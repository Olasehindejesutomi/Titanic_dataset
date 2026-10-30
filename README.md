Titanic Survival Prediction
Project Overview
This project uses machine learning to predict whether a passenger
survived the Titanic disaster based on selected passenger information.
The work is documented in the Jupyter Notebook Titanic_dataset.ipynb.

The notebook explores the dataset, prepares the selected features,
trains classification models, compares their performance, and tunes
Decision Tree and Random Forest models using GridSearchCV.
Project Objective
Build classification models that predict the Survived outcome using
passenger class, sex, age, family-travel information, and fare.
Dataset Description
The notebook reads the dataset from:
pd.read_csv('data/titanic.csv')
The dataset inspected in the notebook contains 887 rows and 8
columns.
  Column                              Description
  Survived                          Target variable: 0 = did not
survive, 1 = survived

  Pclass                            Passenger ticket class (1, 2, or 3)

  Name                              Passenger name

  Sex                               Passenger sex (male or female)

  Age                               Passenger age

  SibSp                             Number of siblings or spouses
aboard

  PaCh                              Number of parents or children
aboard, using the column name in
this dataset
Fare                              Passenger fare
Dataset observations
- Total records: 887
- Total columns: 8
- Missing values: None in the inspected dataset
- Passengers who did not survive (Survived = 0): 545
- Passengers who survived (Survived = 1): 342
The notebook uses six features for modelling: Pclass, Sex, Age,
SibSp, PaCh, and Fare. The Name column is not included in the
model features.

Tools and Libraries
- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Seaborn (used to load an additional built-in Titanic dataset for
  reference)
Project Workflow
1. Import libraries -- Load the Python libraries used for data
   handling, visualization, model training, and evaluation.
2. Load the data -- Read data/titanic.csv into a Pandas
   DataFrame.
3. Explore the data -- Inspect the dataset structure, descriptive
   statistics, survival counts, and missing values.
4. Visualize the target -- Plot the distribution of passengers who
   survived and those who did not.
5. Select features and target -- Use Pclass, Sex, Age,
   SibSp, PaCh, and Fare as input features, with Survived as
   the target.
6. Encode the categorical feature -- Convert Sex to numeric
   values: female = 1 and male = 0.
7. Split the data -- Use an 80/20 train-test split with
   random_state=42 and stratification.
8. Scale features -- Apply StandardScaler to the training and
   test features for Logistic Regression. The scaler is fitted on the
   training data and applied to the test data.
9. Train classification models -- Train Logistic Regression,
   Decision Tree, and Random Forest classifiers.
10. Evaluate models -- Compare accuracy and review classification
    reports.
11. Tune hyperparameters -- Use five-fold GridSearchCV to tune
    Decision Tree and Random Forest models.
12. Make a sample prediction -- Use the tuned Random Forest model to
    predict survival for a passenger example.
Machine Learning Models
The notebook trains and evaluates the following classifiers:
- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier

Model Results
  Model                   Test accuracy
  Logistic Regression            76.97%
Decision Tree                  80.34%
Random Forest                  80.90%
Hyperparameter tuning
GridSearchCV uses five-fold cross-validation and accuracy as the scoring
metric.
  Model           Best parameters                     Best  Test accuracy after
cross-validation               tuning
accuracy 
  Decision Tree   max_depth=4                     81.81%               80.34%
Random Forest   max_depth=7,                    83.92%               80.34%
n_estimators=50
The tuned Random Forest achieved the highest cross-validation accuracy
among the tuned models in this notebook. Its test accuracy was 80.34%.

Project Purpose
This is an educational machine learning project demonstrating
exploratory data analysis, categorical encoding, feature scaling,
train-test splitting, classification, model evaluation, and
hyperparameter optimization.
Disclaimer
This project is for educational purposes only. The predictions are
generated from patterns learned from the dataset and should not be
interpreted as definitive historical conclusions about individual
passengers.
