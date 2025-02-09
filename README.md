# Future Value Insights (CLTV)

This project aims to predict Customer Lifetime Value (CLTV) using machine learning. CLTV represents the total revenue a business can expect from a customer over their entire relationship. The goal is to identify high-value customers and optimize business strategies for retention and growth.

## Table of Contents

1. [Overview](#overview)
2. [Dataset Source](#dataset-source)
3. [Key Columns](#key-columns)
4. [Project Structure](#project-structure)
5. [Key Features and Methods](#key-features-and-methods)
6. [Technologies Used](#technologies-used)
7. [Installation](#installation)
8. [Key Results](#key-results)
   

## Overview

CLTV prediction helps businesses identify and focus on high-value customers, leading to improved retention and growth strategies. This project leverages machine learning to build models that predict CLTV.

## Dataset Source
Download the dataset from [Kaggle](https://www.kaggle.com/datasets/shibumohapatra/customer-life-time-value).

## Key Columns

- **CustomerID:** Unique identifier for each customer
- **Income:** Annual income of the customer
- **Vintage:** Duration of relationship with the customer
- **Claim_Amount:** Total claim amount made by the customer
- **Channel:** Marketing or acquisition channel
- **Customer_Segment:** Segmentation based on various criteria
- **CLTV:** Customer Lifetime Value (target variable)
- **Marital_status** : Marital Status of the customer {0:Single, 1: Married}.
- **Num_policies** : Total no. of policies issued by the customer.
- **Policy** : Active policy of the customer.
- **Type_of_policy** : Type of active policy.

## Project Structure

```
cltv-project/
├── data/
│   └── raw_data/
│       └── Future_Value_Insights_data.csv  # Source: Kaggle
├── notebook/
│   ├── 1_data_preprocessing.ipynb         # Data checks & cleaning
│   ├── 2_EDA.ipynb                        # Exploratory Data Analysis
│   └── 3_model_building.ipynb             # Model training & evaluation
└── requirements.txt                       # Dependencies
```

## Key Features and Methods

1. **Data Preprocessing** (`1_data_preprocessing.ipynb`):
   - Handled null values and inconsistencies in the dataset.
   - Encoded categorical variables and normalized numerical data.

2. **Exploratory Data Analysis** (`2_EDA.ipynb`):
   - Investigated distributions, correlations, and key patterns in the data.
   - Identified key factors influencing customer lifetime value.

3. **Model Building** (`3_model_building.ipynb`):
   - Created new features such as interaction terms and ratios. 
   - Encodes categorical features and scales numerical data.
   - Trains and evaluates 4 models: Linear Regression, KNN, Decision Tree, and Random Forest.
   - Evaluated performance using RMSE and R² scores.

## Technologies Used

- **Python Libraries:** pandas, numpy, scikit-learn, matplotlib, seaborn
- **Jupyter Notebook:** For interactive data exploration and analysis

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Santheeppa/Future-Value-Insights-CLTV.git
   cd Future-Value-Insights-CLTV
   ```
2. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Key Results
- **Top Features**: `income`, `vintage`, and `claim_amount` were critical predictors.
- **Model Performance**:
  | Model               | RMSE       | R² Score   |
  |---------------------|------------|------------|
  | Decision Tree       | 82,594.77  | 0.152      |
  | Random Forest       | 82,658.16  | 0.151      |
  | Linear Regression   | 82,704.66  | 0.150      |
  | KNN                 | 85,997.40  | 0.081      |


