# Titanic-Survival-Prediction
Project Objective
The goal of this project is to build a machine learning model to predict whether a passenger survived the Titanic disaster. Using the Titanic dataset, we analyze various features such as age, gender, passenger class, and ticket fare to classify passengers into "survived" or "not survived."

Dataset Description
The dataset contains information about passengers aboard the Titanic. Key features include:

Survived: Target variable (1 = survived, 0 = not survived).
Pclass: Passenger class (1st, 2nd, 3rd).
Sex: Gender of the passenger.
Age: Age of the passenger.
SibSp: Number of siblings/spouses aboard.
Parch: Number of parents/children aboard.
Fare: Ticket price paid.
Embarked: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton).
The dataset includes some missing values, particularly for the Age and Cabin columns, which need to be addressed during preprocessing.

Preprocessing Steps
Exploratory Data Analysis (EDA):

Analyzed survival rates across features like gender, class, and age.
Visualized data distributions using histograms and bar plots.
Handling Missing Data:

Imputed missing Age values with the median age based on Pclass and Sex.
Dropped the Cabin column due to a high proportion of missing data.
Filled missing Embarked values with the mode.
Encoding Categorical Variables:

Converted Sex and Embarked into numerical variables using one-hot encoding.
Feature Scaling:

Normalized the Fare and Age columns to bring them to the same scale.
Data Splitting:

Split the dataset into training (80%) and testing (20%) sets for model evaluation.
Feature Engineering
Created a new feature, FamilySize, as SibSp + Parch + 1 to analyze the impact of family presence on survival.
Created a binary feature IsAlone, indicating whether the passenger was traveling alone or not.
Categorized Fare into bins (low, medium, high) to capture non-linear relationships.
Model Training and Results
Models Used:

Logistic Regression
Random Forest Classifier
Gradient Boosting Classifier (e.g., XGBoost)
Evaluation Metrics:

Accuracy
Precision, Recall, F1-Score
Confusion Matrix and ROC-AUC Curve
Best Model Performance:

Model: Gradient Boosting Classifier
Accuracy: 85%
F1-Score: 0.82
ROC-AUC: 0.87
The Gradient Boosting Classifier performed best, balancing recall and precision effectively.

Challenges Faced
Handling Missing Values:

The Age and Cabin columns contained significant missing values. Imputation strategies were explored to minimize data loss.
Class Imbalance:

The dataset was slightly imbalanced, with more passengers who did not survive. Techniques like stratified sampling were applied during data splitting.
Feature Selection:

Determining the most important features, such as Pclass and Sex, required extensive EDA and feature importance analysis.
Key Insights
Gender and Class Influence Survival:

Female passengers had a significantly higher survival rate than males.
Passengers in 1st class were more likely to survive compared to those in 2nd and 3rd classes.
Family Matters:

Passengers traveling with family members had a higher chance of survival compared to those traveling alone.
Fare Correlation:

Higher ticket fares were generally associated with a higher probability of survival.
How to Run the Code
Clone this repository:
bash
Copy code
git clone https://github.com/your-username/titanic-survival-prediction.git
Navigate to the repository:
bash
Copy code
cd titanic-survival-prediction
Install required dependencies:
Copy code
pip install -r requirements.txt
Run the notebook or script:
Copy code
jupyter notebook Titanic_Survival_Prediction.ipynb
