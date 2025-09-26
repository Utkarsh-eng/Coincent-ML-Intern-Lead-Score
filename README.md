# Lead Scoring Case Study

## Project Overview

This project focuses on building a logistic regression model to assign a lead score to potential customers for an education company. The goal is to help the sales team identify "hot leads" - those with a higher probability of converting - so they can focus their efforts more effectively and improve the overall lead conversion rate.

## Problem Statement

An education company, X Education, is struggling with a low lead conversion rate of around 38%. They receive a large number of leads from various sources, and their sales team is not able to effectively prioritize which leads to follow up with. This project aims to create a lead scoring model that will rank leads based on their likelihood of conversion, enabling the sales team to target the most promising prospects.

## Dataset

The dataset used for this project is `Leads.csv`, which contains information about the leads acquired by the company. The dataset includes a variety of attributes for each lead, such as:
- Lead Origin and Source
- Demographic information (Country, City, Occupation)
- Website activity (Total Visits, Time Spent on Website, Page Views Per Visit)
- Past interactions (Last Activity)
- The target variable, `Converted`, which indicates whether a lead was successfully converted or not.

## Methodology

The project follows a structured data science workflow:

1.  **Data Cleaning and Preparation:**
    - The raw data is cleaned to handle missing values, inconsistencies, and irrelevant information.
    - Categorical variables are converted into a numerical format using one-hot encoding (dummy variables).

2.  **Exploratory Data Analysis (EDA):**
    - A thorough EDA is conducted to understand the data distribution and the relationships between different variables and the conversion status.
    - Visualizations are used to identify key factors that influence lead conversion.

3.  **Model Building:**
    - The data is split into training and testing sets.
    - Numerical features are scaled using MinMaxScaler.
    - **Recursive Feature Elimination (RFE)** is employed for feature selection to identify the most predictive variables.
    - A **Logistic Regression** model is built using the selected features with the `statsmodels` library.

4.  **Model Evaluation:**
    - The model's performance is evaluated using metrics like Accuracy, Sensitivity, Specificity, and Precision.
    - The **ROC curve** and **Precision-Recall curve** are analyzed to determine the optimal probability cutoff for classifying leads.

5.  **Lead Scoring:**
    - The final model is used to predict the conversion probability for each lead.
    - These probabilities are then converted into a lead score between 0 and 100.

## Conclusion

The logistic regression model developed in this project provides a reliable way to score leads based on their conversion potential. By using the lead scores, the sales team can prioritize their efforts on high-scoring leads, which is expected to lead to a significant improvement in the lead conversion rate and overall sales efficiency.

## How to Run the Project

1.  **Prerequisites:**
    - Python 3.x
    - Jupyter Notebook
    - Required Python libraries: pandas, numpy, scikit-learn, statsmodels, matplotlib, seaborn

2.  **Installation:**
    ```bash
    pip install pandas numpy scikit-learn statsmodels matplotlib seaborn
    ```

3.  **Running the Notebook:**
    - Clone or download this repository.
    - Place the `Leads.csv` file in the same directory as the Jupyter notebook.
    - Open and run the `Lead_Score_Case_Study.ipynb` notebook in a Jupyter environment.
