# **Customer Churn Prediction - Telecom Dataset**  

## **Project Overview**  
This project analyzes customer data from a telecommunications company to predict **customer churn**—the likelihood that a customer will discontinue their service. By identifying key churn indicators, the company can **develop targeted strategies to improve customer retention and enhance customer satisfaction.**  

---

## **Dataset Source**  
- **Name:** Telco Customer Churn Dataset  
- **Source:** [Kaggle - Telco Customer Churn Dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)  
- **Number of Records:** 7,043 customers  
- **Number of Features:** 21 columns, including **demographic, service, and account information**  

---

## **Data Dictionary**  
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

## **Project Objectives**
- Perform **Exploratory Data Analysis (EDA)** to understand customer behavior and churn drivers.  
- Engineer relevant features to enhance model performance.  
- Build and evaluate multiple **classification models** to predict customer churn.  
- Compare model performance across various feature sets.  
- Provide **business recommendations** to reduce churn and improve retention strategies.  

---

## **Tools & Technologies**
- **Programming Language:** Python  
- **Libraries Used:**  
  - Data Manipulation: Pandas, NumPy  
  - Visualization: Matplotlib, Seaborn  
  - Machine Learning: Scikit-learn, Imbalanced-learn  

---

## **Feature Engineering**
To improve model performance, **feature transformations** were applied:
1. **One-Hot Encoding**: Categorical variables like `Contract`, `PaymentMethod`, and `InternetService` were converted into multiple binary columns.  
2. **Binning**:  
   - **Tenure** was grouped into **three categories**: `0-6 months`, `6-12 months`, and `12+ months`.  
   - **New features** were created for better interpretability:
     - `LongTermContract`: Customers with **one-year or two-year contracts**.  
     - `ManualPay`: Customers paying via **manual methods** (e.g., mailed or electronic check).  
     - `Has_Internet`: Customers with **internet service**.  
     - `TotalStreamingServices`: Count of streaming services subscribed to.  
     - `TotalSecurityServices`: Count of security/support services subscribed to.  
3. **Log Transformations**: Applied to **right-skewed numerical features** like `MonthlyCharges` to normalize distributions.  

---

## **Modeling & Evaluation**
The following **four classification models** were tested using various feature sets:

| Model                 | Best Feature Set        | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|----------------------|-----------------------|---------|-----------|--------|----------|---------|
| **Logistic Regression** | One-Hot Encoded Features | 0.737   | 0.503     | 0.805  | 0.619    | 0.835   |
| **KNN**               | Log + Binned Features  | 0.705   | 0.464     | 0.722  | 0.565    | 0.776   |
| **Decision Tree**     | Fully Engineered Features | 0.727   | 0.490     | 0.754  | 0.594    | 0.802   |
| **Random Forest**     | Fully Engineered Features | 0.751   | 0.518     | 0.792  | 0.630    | 0.845   |

**Final Model Selection:** **Random Forest with Fully Engineered Features**  
- **Best overall performance** (Highest ROC-AUC: **0.845**)  
- **Balances recall (0.792) and precision (0.518)**  
- **Leverages multiple feature transformations for improved accuracy**  

---

## **Business Insights & Recommendations**
The churn analysis revealed key business insights:

### **1Tenure Significantly Affects Churn**
- **Short tenure (<6 months) customers churn the most.**
- **Recommendation:** Implement **onboarding incentives and personalized customer engagement** for new customers.  

### **Contract Type Influences Loyalty**
- **Month-to-month contracts** have the **highest churn rates**.  
**Recommendation:** Encourage **long-term contracts** by offering **discounts & loyalty perks**.  

### **Internet & Streaming Services Impact Retention**
- **Fiber optic customers churn more frequently** (likely due to pricing).  
- Customers **bundling security/streaming services are more likely to stay.**  
**Recommendation:** Offer **discounted bundle packages** for **streaming & security services**.  

### **Payment Method Correlates with Churn**
- **Customers paying via electronic check churn more** than those using auto-pay methods.  
**Recommendation:** **Incentivize automatic payments** with small discounts or bonus perks.  

### **High Monthly Charges Increase Churn Risk**
- **Customers with higher bills are more likely to leave.**
- **Recommendation:** Offer **tiered pricing models** with **customized payment plans** to retain price-sensitive customers.  

---

## **Final Conclusion**
This **churn prediction model** helps the business proactively identify customers **at high risk of leaving**.  
By implementing **targeted retention strategies**, the company can:  
Reduce customer churn  
Improve customer satisfaction  
Maximize long-term revenue growth  

This project **combines machine learning with actionable business recommendations**, demonstrating how **data-driven insights can drive retention strategies in telecom industries.** 

