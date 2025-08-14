# 📈 Machine Learning – Customer Churn Prediction  

## 📌 Overview  
This folder contains the complete machine learning workflow for predicting customer churn using the **Telco Customer Churn dataset**.  
It covers **data preprocessing, feature engineering, model training, evaluation, and insights** — providing a structured approach to solving classification problems in a business context.  

---

## 🛠 Tools & Libraries Used  
- **Python:** Core programming language for analysis and modeling  
- **Pandas / NumPy:** Data manipulation and numerical operations  
- **Matplotlib / Seaborn:** Data visualization for EDA  
- **Scikit-learn:** Preprocessing, model training, and evaluation  
- **XGBoost:** Gradient boosting classifier for high-performance modeling  

---

## 🔍 Project Workflow  
1. **Data Loading & Cleaning**  
   - Identified missing values and handled inconsistencies  
   - Converted `TotalCharges` from string to numeric format  

2. **Exploratory Data Analysis (EDA)**  
   - Analyzed churn distribution and correlations between features  
   - Visualized categorical and numerical feature distributions  

3. **Feature Encoding & Scaling**  
   - One-hot encoded categorical variables  
   - Scaled numerical features using `StandardScaler` (binary features excluded from scaling)  

4. **Class Imbalance Handling**  
   - Applied **SMOTE** to balance churn (`Yes`/`No`) distribution  

5. **Model Training & Evaluation**  
   - Trained **Logistic Regression**, **Random Forest**, and **XGBoost**  
   - Evaluated performance using **Accuracy** and **ROC–AUC**  

---

## 📊 Model Performance Summary  
| Model                | Accuracy | ROC–AUC |
|----------------------|----------|---------|
| Logistic Regression  | 0.7331   | 0.8214  |
| Random Forest        | **0.7665**   | **0.8245**  |
| XGBoost              | 0.7537   | 0.8181  |

**Key Findings:**
- **Random Forest** achieved the highest accuracy (**0.7665**) and ROC–AUC (**0.8245**), making it the top-performing model for this dataset.  
- **Logistic Regression** performed surprisingly well despite its simplicity — just 0.003 ROC–AUC lower than Random Forest.  
- **XGBoost** slightly underperformed, likely due to the dataset’s relatively small size and Random Forest’s ability to handle the feature space without heavy tuning.  

**Conclusion:**  
With a **small, class-imbalanced dataset**, achieving above **80% ROC–AUC** is acceptable.  
For higher accuracy (e.g., ~95%), the following improvements could be considered:  
- Acquiring more data  
- Hyperparameter tuning and feature selection  
- Using stacking/ensemble methods to combine model strengths  

---

## 📁 Files in this Folder  
- **Customer_Churn_Prediction.ipynb** – Jupyter Notebook containing the full ML workflow  
- **Customer_Churn_Prediction.pdf** – PDF export of the notebook for quick review  
