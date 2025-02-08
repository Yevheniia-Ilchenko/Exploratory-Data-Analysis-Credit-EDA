# EDA of Credit Issuance and Repayment Dataset

## Overview
This project performs **Exploratory Data Analysis (EDA)** on a dataset related to credit issuance and repayment by customers. The goal is to uncover insights about customer behavior, identify key factors influencing credit repayment, and detect any trends or anomalies in the data.  
**Dataset has  ~307k rows та 122 columns**.


![image](https://github.com/user-attachments/assets/a6f2c789-f851-4d58-8281-2411d3c447fa)


---

### **1. Understanding the Business Problem**
- Define project goals and key questions to answer:
  - What factors influence loan repayment behavior?
  - How do customer demographics relate to credit defaults?
- Understand how the analysis results will be utilized:
  - Insights can guide credit policies and improve risk assessment models.

---

### **2. Data Collection and Integration**
- Gather the necessary datasets:
  - `credit_data.csv` (primary dataset).
- Validate completeness and quality of data sources.
- Integrate data from multiple sources if applicable.

---

### **3. Initial Data Review**
- Assess dataset size and structure:
  - The dataset contains customer-level and loan-level information in tabular format.
- Identify variable types:
  - **Categorical variables**: 16 categorical
 
   ![image](https://github.com/user-attachments/assets/8b9089b8-359b-486e-acf3-c7bead3b6a6b)


  - **Numerical variables**: 106 numerical
 
  ![image](https://github.com/user-attachments/assets/9a659586-0e49-49fc-acbe-08706217f7cd)

  

#### Analysis of Variable Types:
- **Categorical variables**:
  - Identify unique categories and their distributions.
  - Check for ordinal variables that may require special encoding.
- **Numerical variables**:
  - Analyze distributions (normality, skewness).
  - Identify potential correlations with the target variable (`repayment_status`).
  - Highlight features with high variability that could be useful for modeling.
- **Time variables**:
  - Understand the temporal range and possible effects on the target variable.

---

### **4. Data Cleaning**
- Handle missing values: 67 columns

 ![image](https://github.com/user-attachments/assets/8731c74b-46ba-4973-97d5-a2f3fede619f)



- Correct or remove anomalies and outliers
- Remove duplicates

---

### **5. Data Analysis and Visualization**
- Analyze the distribution of each variable:
  - Distribution of `repayment_status` (Paid, Late, Default).
  - Correlation between `customer_income` and `credit_score`.
- Visualize distributions and relationships:
  - **Correlation heatmap**: Understand relationships between numerical variables.
  - **Time-based trends**: Plot repayment trends over time.
  - **Income vs Defaults**: Visualize default rates by income levels.
- Identify correlations between features:
  - High correlations may indicate multicollinearity, which needs to be addressed.
 
![image](https://github.com/user-attachments/assets/458e96fe-c69c-4687-aa09-e6db8d629360)

![image](https://github.com/user-attachments/assets/b6c05691-3f2e-4d70-80af-6d165d64bc60)

![image](https://github.com/user-attachments/assets/21642dbf-734f-443a-854f-83cef003e55c)

![image](https://github.com/user-attachments/assets/84cc2b11-97cb-4d30-9700-e4f7b7bafead)

![image](https://github.com/user-attachments/assets/f8581c0f-b8a2-4a9e-870d-b3673a70637d)

![image](https://github.com/user-attachments/assets/b4c99fca-84a8-4542-b1bd-f6876e69c5c8)





---

### **6. Feature Engineering**
- Create new features:
  - Example: `repayment_delay` = `repayment_date` - `due_date`.
- Select or discard features for modeling:
  - Retain features with high predictive potential.
- Encode categorical variables:
  - Apply one-hot encoding for `region`.
- Normalize or standardize numerical variables:
  - Standardize `credit_amount` and `customer_income` for consistent scaling.

---



---

## Copy and install 
Copy this project:
```
git clone https://github.com/username/EDA_Credit_Project.git
```

To run this project, install the following dependencies:

```
pip install pandas numpy matplotlib seaborn jupyterlab
```
