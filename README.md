💎 Diamonds Machine Learning Project
📌 Overview

This project analyzes the Diamonds Dataset, which contains 53,940 diamond records with multiple numerical and categorical features. The objective is to explore the dataset, understand relationships between variables, and build machine learning models for both classification and regression tasks.

The project includes:

Exploratory Data Analysis (EDA)
Feature Engineering
Data Preprocessing
Classification Models
Regression Models
Cross‑Validation and Model Evaluation
📊 Dataset Information

The dataset contains the following features:

Feature	Description
carat	Weight of the diamond
cut	Quality of the cut
color	Diamond color grade
clarity	Diamond clarity grade
depth	Total depth percentage
table	Width of top of diamond
price	Price in USD
x	Length in mm
y	Width in mm
z	Depth in mm

Total entries: 53,940

🔍 Exploratory Data Analysis (EDA)

EDA was performed to:

Understand feature distributions
Identify correlations
Detect outliers
Explore relationships between variables

Key Findings:

Carat has a strong positive correlation with price
Some features show strong relationships with price and cut
Data distribution varies across categorical variables

Visualizations Used:

Histograms
Scatter plots
Box plots
Correlation heatmap
⚙️ Feature Engineering

A new feature was created:

data["data_table_ratio"] = data["depth"] / data["table"]
Why?
Capture geometric proportions
Improve model performance
Reveal hidden relationships
🔄 Data Preprocessing
Encoding Categorical Variables

Machine learning models require numerical input. Label Encoding was applied to:

cut
color
clarity
from sklearn.preprocessing import LabelEncoder
🤖 Machine Learning Models
Classification Task

Goal: Predict diamond cut quality

Models Used:

Decision Tree Classifier
Random Forest Classifier

Evaluation Metrics:

Precision
Recall
F1 Score
Accuracy
Decision Tree Results
Metric	Score
Precision	0.706
Recall	0.705
F1 Score	0.705
Random Forest (Cross‑Validation)
Metric	Score
Precision	0.784
Recall	0.762
F1 Score	0.770
📈 Regression Task

Goal: Predict diamond price

Models Used:

Random Forest Regressor
Linear Regression
Random Forest Regression

Mean Squared Error:

303638.09
Linear Regression

Mean Squared Error:

1293191.7

Random Forest performed significantly better than Linear Regression.

🔁 Cross Validation

Cross-validation was applied using:

K‑Fold
Stratified K‑Fold

Benefits:

More reliable evaluation
Reduces overfitting
Uses full dataset effectively

🛠️ Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit‑learn

▶️ Usage

Run the notebook or Python script:

python diamonds_project.py


📊 Results Summary
Model	Task	Performance
Decision Tree	Classification	F1 ≈ 0.705
Random Forest	Classification	F1 ≈ 0.77
Random Forest	Regression	Best Performance
Linear Regression	Regression	Higher Error

🚀 Future Improvements
Hyperparameter tuning
Feature selection
Deep learning models
Deployment (Streamlit / Flask)


This project is open source and available under the MIT License.

⭐ If you found this project helpful, feel free to star the repository!
