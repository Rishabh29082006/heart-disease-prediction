# heart-disease-prediction
Heart Disease Prediction Analysis
This repository contains a Jupyter/Google Colab notebook for an initial exploration and predictive modeling of a heart disease dataset. The analysis covers data loading, initial inspection, exploratory visualization, data preprocessing, and the implementation of a basic Logistic Regression model.

📊 Dataset Overview
The project analyzes two datasets, with the primary work focusing on a dataset loaded as df1 (Heart_Disease_Prediction.csv).

df1 (Heart_Disease_Prediction.csv)
Detail	Value
Total Entries	
270 

Total Columns	
14 

Missing Values	
None (All columns have 270 non-null counts) 


Target Variable		
Heart Disease (Object type, converted to numerical) 






Export to Sheets
The dataset contains features like Age, Sex, Chest pain type, BP, Cholesterol, Max HR, etc. .

Key Statistics for df1 (Heart Disease Data)
Feature	Mean	Standard Deviation (σ)	Min	Max
Age		
54.43 



9.11 



29.00 



77.00 



BP (trestbps)		
131.34 



17.86 



94.00 



200.00 



Cholesterol		
249.66 



51.69 



126.00 



564.00 



Max HR (thalach)		
149.68 



23.17 



71.00 



202.00 




Export to Sheets
💻 Analysis and Modeling Steps
1. Data Loading and Initial Inspection
The dataframes were loaded using pandas.read_csv.



df.describe() and df.info() were used to check statistics and data types .



Missing values were checked using df1.isnull().sum(), which returned 0 for all columns .

The number of unique values for each feature was also checked using df1.nunique() .

2. Exploratory Data Analysis (EDA)
A scatterplot was generated using seaborn to visualize the relationship between Age and Max HR (Maximum Heart Rate), colored by the Heart Disease outcome .

3. Preprocessing and Encoding
The categorical target column, 'Heart Disease' (with values 'Presence' and 'Absence' ), was converted to a numerical format (likely 1 and 0) using LabelEncoder from sklearn.preprocessing .





Features (X) and the target (y) were separated.


StandardScaler was applied to the training and testing feature data to normalize the features .

4. Model Implementation
The data was split into training and testing sets using train_test_split.

The test size was set to a non-standard value (or a typo exists in the notebook) test_size=8.2.

A random_state=42 was used for reproducibility.

A Logistic Regression model was imported from sklearn.linear_model.

The model was initialized and trained using the scaled training data (x_train, y_train).

🛠️ Key Libraries Used

pandas (as pd)  - For data manipulation and analysis.





seaborn (as sns) and matplotlib.pyplot (as plt)  - For data visualization.





sklearn.preprocessing.LabelEncoder and sklearn.preprocessing.StandardScaler  - For data encoding and scaling.



sklearn.model_selection.train_test_split  - For splitting data.


sklearn.linear_model.LogisticRegression  - For model implementation.

