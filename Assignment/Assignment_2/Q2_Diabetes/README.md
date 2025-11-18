# Diabetes Analysis

## Project Overview
This project focuses on predicting the onset of diabetes based on diagnostic medical data. It is a classic binary classification problem using Diabetes Dataset. The goal is to build a model that can accurately predict whether a patient has diabetes (Outcome = 1) or not (Outcome = 0) based on several medical predictor variables. The main objectives analyze the effects of sampling variablities.

## Repository Structure

```
Q2_Diabetes/
├── clean_data                 	   	 # Processed and cleaned dataset
│   ├── clean_data.csv           
├── raw_data						 # Original dataset
│   ├── diabetes.csv   		    
│   └── metadata.txt
├── results/                 		 # Output results and visualization
│   ├── comparison_plot.png  
├── src/   
│   └── Assignment2_Diabetes.ipynb 
└── Assignment2_Diabetes_Report.docx # Report and finding documentation
└── README.md                 		 # Project overview and documentation

```

## Key Task & Analysis

This dataset is ideal for several key data science tasks:

- **Binary Classification**: Training machine learning models (e.g., Logistic Regression, Random Forest, SVM) to predict the Outcome variable.

- **Exploratory Data Analysis (EDA)**: Analyzing the distributions of features like Glucose, BMI, and Age and their correlation with diabetes.

- **Feature Importance**: Identifying which medical factors (Glucose, BMI, Age, Pregnancies, etc.) are the most significant predictors of diabetes.

- **Data Preprocessing**: Handling potential missing values (often represented as 0 in this dataset for columns like Glucose or BMI) and scaling features for modeling.

## Dataset Description

- **File**: raw_data/metadata.txt
- **Source**: This is the Pima Indians Diabetes Dataset, originally from the National Institute of Diabetes and Digestive and Kidney Diseases.
- **Description**: This dataset contains 768 entries (all female participants of Pima Indian heritage) with 8 medical predictor variables and 1 target variable (Outcome)

## Installation / Setup

- **Requirement**: None
- **Enviroment**: This assignement was built using R. Change runtime in Google Colab by choosing Runtime > Change runtime type > Click on down arrow under Runtime type > Select R > Click Save

## How to Run the Project

**1.** Open the notebooks in [src/*.ipynb](https://github.com/mosomo82/COMP_SCI_5530/blob/main/Assignment/Assignment_2/Q2_Diabetes/src/Assignment2_Diabetes.ipynb) (e.g. in Google Colab) to explore data and visualizations.
**2.** Run top-to-bottom. Output will be saved locally to see the analysis and findings. 

## Future Work/Next Steps:

- Conduct more extensive hyperparameter search (Random Forest etc.)
- Combine more predictions(e.g. Logistic Regression, and Random Forest) using a classifier or stacking

## License

## Authors/Contributors:

- **Tony Nguyen** - [Github Profile](https://github.com/mosomo82)

## Acknowledgements

- This dataset is courtesy of the National Institute of Diabetes and Digestive and Kidney Diseases.
- Special thanks to Professor. Shah  for guidance on the project.

