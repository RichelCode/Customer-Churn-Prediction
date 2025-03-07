# Customer Churn Prediction - Telecom Dataset

## Project Overview
This project aims to analyze customer data from a telecommunications company to predict customer churn — the likelihood that a customer will discontinue their service. By understanding which factors contribute to churn, the company can develop targeted strategies to improve customer retention and customer satisfaction.

## Dataset Source
- **Name:** Telco Customer Churn Dataset
- **Source:** [Kaggle - Telco Customer Churn Dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Number of Records:** 7,043 customers
- **Number of Features:** 21 columns including demographic, service, and account information.

---

## Data Dictionary
| Column Name           | Description                                                                 | Data Type      |
|----------------------|-----------------------------------------------------------------------------|------------------|
| **customerID**        | Unique identifier for each customer                                        | String          |
| **gender**            | Gender of the customer (`Male` / `Female`)                                 | Categorical     |
| **SeniorCitizen**     | Indicates if the customer is a senior citizen (1 = Yes, 0 = No)            | Integer         |
| **Partner**           | Whether the customer has a partner (`Yes` / `No`)                          | Categorical     |
| **Dependents**        | Whether the customer has dependents (`Yes` / `No`)                         | Categorical     |
| **tenure**             | Number of months the customer has been with the company                    | Integer         |
| **PhoneService**      | Whether the customer has phone service (`Yes` / `No`)                      | Categorical     |
| **MultipleLines**     | Whether the customer has multiple phone lines                              | Categorical     |
| **InternetService**   | Type of internet service (`DSL`, `Fiber optic`, `No`)                      | Categorical     |
| **OnlineSecurity**    | Whether the customer has online security services (`Yes`, `No`, `No internet service`) | Categorical |
| **OnlineBackup**      | Whether the customer has online backup services (`Yes`, `No`, `No internet service`) | Categorical |
| **DeviceProtection**  | Whether the customer has device protection services                        | Categorical     |
| **TechSupport**       | Whether the customer has tech support services                             | Categorical     |
| **StreamingTV**       | Whether the customer has streaming TV services                             | Categorical     |
| **StreamingMovies**   | Whether the customer has streaming movie services                          | Categorical     |
| **Contract**          | Type of customer contract (`Month-to-month`, `One year`, `Two year`)       | Categorical     |
| **PaperlessBilling**  | Whether the customer has paperless billing                                 | Categorical     |
| **PaymentMethod**     | Payment method used by the customer (`Electronic check`, `Mailed check`, `Bank transfer`, `Credit card`) | Categorical |
| **MonthlyCharges**    | Monthly charges incurred by the customer                                   | Float           |
| **TotalCharges**      | Total charges incurred by the customer during their tenure                 | Float (with some missing) |
| **Churn**             | Target variable: whether the customer churned (`Yes` / `No`)                | Categorical     |

---

## Project Objectives
- Perform **Exploratory Data Analysis (EDA)** to understand customer behavior and churn drivers.
- Engineer relevant features where necessary.
- Build and evaluate **classification models** to predict customer churn.
- Provide **business recommendations** to reduce churn and improve customer retention.

---

## Tools & Technologies
- Python
- Libraries: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn

---

## Project Workflow
1. **Data Understanding** (including reviewing this Data Dictionary)
2. **Data Cleaning & Preprocessing** (handling missing values, encoding categorical variables, etc.)
3. **Exploratory Data Analysis (EDA)** (visualizations & insights)
4. **Modeling** (training classification models such as Logistic Regression, Decision Trees, Random Forest, etc.)
5. **Evaluation & Interpretation** (measuring accuracy, precision, recall, F1-score, etc.)
6. **Business Recommendations** (how the company can improve retention based on data insights)

---
