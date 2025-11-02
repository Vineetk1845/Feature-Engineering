🧠 Life Expectancy Prediction – Feature Engineering Project
📘 Overview

This project focuses on data preprocessing and feature engineering using the Life Expectancy Dataset from the World Health Organization (WHO).
The aim is to prepare the data for regression modeling to predict Life Expectancy based on health, economic, and demographic indicators.

📊 Dataset Information

Dataset name: Life Expectancy Data
Source: WHO / Kaggle
Total rows: 2938
Columns: 22

Target Variable:

Life expectancy (in years)

Key Features:

Country

Year

Status (Developed / Developing)

Adult Mortality

Infant Deaths

BMI

GDP

Schooling

Income Composition of Resources

⚙️ Feature Engineering Steps
1. Data Loading and Exploration

Loaded the dataset using pandas.read_csv().

Checked data types, missing values, and basic statistics.

2. Handling Missing Values

Filled numeric columns with mean values.

Filled categorical columns with mode (most frequent value).

Verified no null values remain after imputation.

3. Encoding Categorical Variables

Converted Country and Status columns into numeric format using Label Encoding from sklearn.preprocessing.

4. Feature Scaling

Applied StandardScaler to normalize all numerical features for better model performance and comparability.

5. Feature Selection

Computed correlation between all features and the target variable (Life expectancy).

Selected only those features with correlation coefficient > 0.3 for better interpretability and accuracy.

6. Optional Dimensionality Reduction (PCA)

Tested Principal Component Analysis to confirm variance distribution and redundancy.

🔍 Observations

No missing data after preprocessing.

Top correlated features: Schooling, Income composition of resources, GDP, BMI, and Adult Mortality.

Scaling improved feature uniformity.

Data is now clean, numeric, and ready for regression modeling.

⚖️ Ethical Discussion

Even though this dataset doesn’t contain personal or sensitive data, ethical issues can still arise.
For example, predicting life expectancy using features like Country, Status, or Income could introduce socioeconomic bias.
To prevent this:

Avoid using sensitive or biased indicators unless necessary.

Test model fairness across countries or income groups.

Use anonymized, balanced data.

Keep models transparent and explainable.

Regularly review and update models to reduce bias.

(https://colab.research.google.com/drive/1pA5INYwSLrYknX1JeAUgjfD4SKIJ8TJr?usp=sharing)
