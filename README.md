# 💳 Loan Default Prediction

A machine learning project that predicts whether a borrower will default on a loan using financial and demographic data. This project compares multiple classification models and evaluates their effectiveness in identifying high-risk borrowers.

🔗 **GitHub Repository:** https://github.com/parinthaokar/-Loan-Default-Prediction  

---

## 📌 Project Overview

Loan default prediction is a critical problem in finance. Accurately identifying high-risk borrowers helps financial institutions:

- Reduce financial losses  
- Improve lending decisions  
- Manage credit risk effectively  

This project frames the problem as a **binary classification task**:
- `0` → No Default  
- `1` → Default  

---

## 📊 Dataset

- Source: Kaggle Loan Dataset  
- Size: **32,586 rows, 13 original features**

### Key Features:
- `customer_age` – Borrower age  
- `customer_income` – Annual income  
- `home_ownership` – Housing status  
- `employment_duration` – Years employed  
- `loan_intent` – Purpose of loan  
- `loan_grade` – Risk classification  
- `loan_amnt` – Loan amount  
- `loan_int_rate` – Interest rate  
- `term_years` – Loan duration  
- `historical_default` – Past defaults  
- `cred_hist_length` – Credit history length  

---

## 🧹 Data Preprocessing

Key preprocessing steps included:

- ✅ Converted string-based numeric fields (e.g., "$", commas) → numeric  
- ✅ Handled missing values:
  - Median imputation (primary)
  - Remaining values filled with 0  
- ✅ One-hot encoding for categorical variables  
- ✅ Removed non-informative features (e.g., `customer_id`)  

📈 Final dataset:
- **21 features after encoding**
- No missing values  

⚠️ Note: Dataset had **class imbalance** (~79% non-default, 21% default)

---

## 🤖 Models Used

Three models were implemented to compare performance:

### 1. Logistic Regression
- Baseline model  
- Simple and interpretable  
- Struggled with convergence (likely due to lack of scaling)

### 2. Decision Tree
- Max depth = 5 (to prevent overfitting)  
- Captures nonlinear relationships  

### 3. Random Forest 🌲 (Best Model)
- 100 trees  
- Ensemble method for improved accuracy and stability  

---

## 📈 Model Performance

| Model                | Accuracy | Precision | Recall | F1 Score |
|---------------------|---------|----------|--------|----------|
| Logistic Regression | 92.02%  | 86.39%   | 73.84% | 79.62%   |
| Decision Tree       | 93.79%  | 94.02%   | 75.36% | 83.66%   |
| Random Forest       | **96.39%** | **97.34%** | **85.25%** | **90.90%** |

### 🏆 Best Model: Random Forest
- Highest accuracy and F1 score  
- Strong balance between precision and recall  
- Most reliable for real-world use  

---

## 🔍 Key Insights

- Most important predictors:
  - Interest Rate  
  - Loan Grade  
  - Income  
  - Employment Duration  

- Model successfully minimized:
  - False negatives (missed defaults)  
  - False positives (incorrect rejections)  

---

## ⚠️ Limitations

- Missing values filled with `0` may introduce bias  
- No feature scaling (impacted logistic regression)  
- No hyperparameter tuning  
- Dataset may not generalize to all populations  

---

## ⚖️ Ethical Considerations

- Risk of bias in financial decision-making  
- Models should **assist, not replace** human judgment  
- Fair lending practices must be maintained  

---

## 🚀 Future Improvements

- Add **feature scaling**  
- Perform **hyperparameter tuning (GridSearchCV)**  
- Use **cross-validation**  
- Test advanced models (e.g., XGBoost)  
- Improve handling of missing values  

---

## 🛠️ Tech Stack

- Python  
- Pandas  
- Scikit-learn  
- NumPy  
- Matplotlib  

---

## 🤝 Acknowledgements

- Dataset: Kaggle Loan Dataset  
- AI Tools:
  - ChatGPT (grammar + assistance)  
  - Gemini (debugging support)  

---

## 📬 Contact

**Parin Thaokar**  
📍 Charlotte, NC  
📧 parinthaokar@gmail.com  
🔗 https://www.linkedin.com/in/parinthaokar  
