Diabetes Dataset EDA
Description
This project performs Exploratory Data Analysis (EDA) on a diabetes dataset. The goal is to explore the characteristics of the data, identify patterns, check for potential anomalies, and conduct statistical analyses to better understand the behavior of the variables.

Dataset
The dataset used is available in diabetes.csv and contains the following columns:

Pregnancies: Number of pregnancies
Glucose: Plasma glucose level
BloodPressure: Diastolic blood pressure
SkinThickness: Skin thickness
Insulin: Insulin level
BMI: Body mass index
DiabetesPedigreeFunction: Diabetes pedigree function
Age: Age of the patient
Outcome: Test result (0 = non-diabetic, 1 = diabetic)
Prerequisites
Python 3.x
Libraries: Pandas, NumPy, Matplotlib, Seaborn, SciPy
Installation Instructions
Install the necessary dependencies using pip:

bash
Copy code
pip install pandas numpy matplotlib seaborn scipy
Data Processing
Before performing the analysis, the dataset is cleaned to remove entries with zero values in the following columns, as zero values are not valid for analysis: Glucose, BloodPressure, SkinThickness, Insulin, and BMI.

python
Copy code
df = df[df['Glucose'] != 0]
df = df[df['BloodPressure'] != 0]
df = df[df['SkinThickness'] != 0]
df = df[df['Insulin'] != 0]
df = df[df['BMI'] != 0]
After cleaning, the dataset contains 392 entries.

Analysis Performed
Data Overview
Dimensions of the DataFrame: 768 rows and 9 columns.
First Entries: Sample of the first 5 entries to understand the structure of the data.
Data Types and Null Values: Checking data types and absence of null values.
Data Cleaning
Removal of Zero Values: Exclusion of zero values in the columns Glucose, BloodPressure, SkinThickness, Insulin, and BMI as these values are invalid.
Descriptive Analysis
Descriptive Statistics: Mean, standard deviation, minimum, and maximum values of the variables.
Patient Distribution: Frequency of diabetic vs. non-diabetic patients.
Visualizations
Age Distribution: Histogram of patient ages.
Relationships Between Variables: Scatter plots and box plots to understand the relationship between variables such as Age, Glucose, Insulin, and Outcome.
Results
The distribution of diabetic patients is approximately 33%, while 67% are non-diabetic.
The histogram shows that most patients are between 20 and 50 years old.
Scatter plots indicate potential correlations between variables like Insulin and Age, and between Glucose and Insulin.
