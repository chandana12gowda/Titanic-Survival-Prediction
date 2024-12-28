# Titanic-Survival-Prediction
Project Objective :
The goal of this project is to build a machine learning model to predict whether a passenger survived the Titanic disaster. Using the Titanic dataset, we analyze various features such as age, gender, passenger class, and ticket fare to classify passengers into "survived" or "not survived."

Dataset Description :
The dataset contains information about passengers aboard the Titanic. Key features include:

Survived: Target variable (1 = survived, 0 = not survived).
Pclass: Passenger class (1st, 2nd, 3rd).
Sex: Gender of the passenger.
Age: Age of the passenger.
SibSp: Number of siblings/spouses aboard.
Parch: Number of parents/children aboard.
Fare: Ticket price paid.
Embarked: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton).

Preprocessing Steps :
Exploratory Data Analysis (EDA):
1. Analyzed survival rates across features like gender, class, and age.
2. Visualized data distributions using histograms and bar plots.
   
Handling Missing Data:
1.Imputed missing Age values with the median age based on Pclass and Sex.
2. Dropped the Cabin column due to a high proportion of missing data.
3. Filled missing Embarked values with the mode.

Encoding Categorical Variables:
1.Converted Sex and Embarked into numerical variables using one-hot encoding.

Feature Scaling:
1.Normalized the Fare and Age columns to bring them to the same scale.

Data Splitting:
1. Split the dataset into training (80%) and testing (20%) sets for model evaluation.

Feature Engineering :
1. Created a new feature, FamilySize, as SibSp + Parch + 1 to analyze the impact of family presence on survival.
2. Created a binary feature IsAlone, indicating whether the passenger was traveling alone or not.
3. Categorized Fare into bins (low, medium, high) to capture non-linear relationships.

Model Training and Results
Models Used:
1. Logistic Regression
2. Random Forest Classifier
3. Gradient Boosting Classifier (e.g., XGBoost)

Evaluation Metrics:
1. Accuracy
2. Precision, Recall, F1-Score
3. Confusion Matrix and ROC-AUC Curve

Best Model Performance:
1. Model: Gradient Boosting Classifier
2. Accuracy: 85%
3. F1-Score: 0.82
4. ROC-AUC: 0.87


Challenges Faced
1. Handling Missing Values:
The Age and Cabin columns contained significant missing values. Imputation strategies were explored to minimize data loss.

2. Class Imbalance:
The dataset was slightly imbalanced, with more passengers who did not survive. Techniques like stratified sampling were applied during data splitting.

3. Feature Selection:
Determining the most important features, such as Pclass and Sex, required extensive EDA and feature importance analysis.
Key Insights

4. Gender and Class Influence Survival:
Female passengers had a significantly higher survival rate than males.
Passengers in 1st class were more likely to survive compared to those in 2nd and 3rd classes.

5. Family Matters:
Passengers traveling with family members had a higher chance of survival compared to those traveling alone.

6. Fare Correlation:
Higher ticket fares were generally associated with a higher probability of survival.


How to Run the Code
1. Clone this repository:
git clone https://github.com/your-username/titanic-survival-prediction.git

2. Navigate to the repository:
cd titanic-survival-prediction

3. Install required dependencies:
pip install -r requirements.txt

5. Run the notebook or script:
jupyter notebook Titanic_Survival_Prediction.ipynb
