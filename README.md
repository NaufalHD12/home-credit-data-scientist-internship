# Home Credit Indonesia - Loan Risk Analysis

## Overview
This project aims to analyze loan risk factors for Home Credit Indonesia by leveraging Exploratory Data Analysis (EDA) and Machine Learning. The goal is to predict loan repayment difficulties based on applicant data, improving risk assessment and decision-making.

## Dataset
The dataset contains customer information, including:
- **Demographics** (Age, Education, Employment Status, etc)
- **Loan Details** (Contract Type, Payment History, etc)
- **Financial Data** (Income, Credit Score, Loan Amount, etc)
- **Behavioral Data** (Employment Duration, Registration Changes, Previous Loan Defaults, etc)

## Exploratory Data Analysis (EDA)
### Key Findings:
- **Loan Difficulties by Age Group:** Mid-career and early-career individuals have the highest loan difficulties.
- **Loan Status by Contract Type:** Cash loans are more common than revolving loans.
- **Education and Loan Status:** Higher education levels correlate with better repayment rates.
- **Employment Duration & Loan Difficulties:** Short employment duration increases the risk of loan difficulties.

## Data Preparation
1. **Handling Missing Values:**
   - Dropped features with >50% missing values.
   - Imputed missing numerical values with the median and categorical values with the most frequent category.
2. **Feature Engineering:**
   - Converted negative time-based features (e.g., DAYS_BIRTH) to positive values.
   - Standardized numerical features and one-hot encoded categorical features.
3. **Feature Selection:**
   - Removed highly correlated features (>0.85 correlation).
   - Used Mutual Information to select the top 30 most relevant features.
4. **Handling Class Imbalance:**
   - Applied **SMOTE (Synthetic Minority Over-sampling Technique)** to balance the dataset.

## Model Training & Evaluation
### **Models Used for Binary Classification:**
- **Logistic Regression**
- **XGBoost**
- **LightGBM**
- **Random Forest**

### **Performance Metrics (Accuracy on Test Set):**
| Model              | Accuracy |
|-------------------|----------|
| Logistic Regression | 0.6855 |
| XGBoost            | 0.9531 |
| LightGBM          | 0.9539 |
| Random Forest      | 0.9591 |

### **Model Selection**
Random Forest was selected for its superior accuracy, outperforming XGBoost and LightGBM. It effectively captures complex patterns in the data while maintaining interpretability.

## Conclusion
The scorecard model provides insights into loan risk factors, helping **Home Credit Indonesia** refine its risk assessment process. Key takeaways:
- Employment duration and education significantly impact loan difficulties.
- Short employment histories and lower education levels increase loan default risk.
- Machine learning models can enhance decision-making, reducing financial risk.


## Author
**Naufal Hadi Darmawan**  
*Data & Machine Learning Specialist*

---
This project serves as a foundation for predictive modeling in the financial sector, helping Home Credit Indonesia optimize loan approval strategies and minimize risks.

