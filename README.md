# 🚀 Kaggle Spaceship Survival Prediction (ML Project)

This project predicts whether a passenger was transported to another dimension in the **Kaggle Spaceship Titanic competition**. The workflow involves data preprocessing, feature engineering, handling missing values, encoding, model training, hyperparameter tuning, and prediction optimization.

---

## 📊 Project Overview
- Goal: Predict passenger transport to another dimension (classification task).  
- Dataset: Provided by Kaggle (*train.csv* & *test.csv*).  
- Approach: Exploratory Data Analysis (EDA), preprocessing, feature engineering, and machine learning models.  

---

## 🛠️ Data Preprocessing
1. **Exploration**: Checked shapes, column types, and missing values.  
2. **Feature Engineering**: Split `PassengerId` into `Group` & `ID`; extracted `Deck`, `CabinNumber`, `CabinSide` from `Cabin`.  
3. **Handling Missing Values**:  
   - Numeric features → Imputed using **KNN Imputer**  
   - Categorical features → Filled using **Mode Imputation**  
4. **Skewness**: Checked for skewness in numerical features; all were <10%, so no transformations were required.  
5. **Encoding**:  
   - One-hot encoding → Nominal features (*HomePlanet, Destination, Deck*)  
   - Label encoding → Binary features (*CryoSleep, VIP, CabinSide*)  
   - Converted all object/boolean columns into numeric types.  

---

## 🤖 Machine Learning Models
Implemented and compared multiple classifiers:
- Logistic Regression  
- K-Nearest Neighbors (KNN)  
- Naive Bayes  
- Decision Tree  
- Support Vector Machine (SVM)  
- Random Forest  
- Gradient Boosting  
- **XGBoost**  

---

## 🔧 Model Tuning & Optimization
- **Hyperparameter Tuning**: Applied `RandomizedSearchCV` on XGBoost.  
- **Threshold Optimization**: Adjusted decision threshold to maximize **F1 Score**, ensuring balanced precision & recall.  

---

## ✅ Best Model
The **tuned XGBoost model** achieved the best performance and was used for generating predictions on the test set.

---

## 📂 Repository Structure
- `ML.py` → Google Colab notebook with full pipeline  
- `submission.csv` → Final Kaggle submission file  
- `README.md` → Project documentation  

---

## 🚀 How to Run
1. Clone this repository  
2. Run the script in Python:  
   ```bash
   python ML.py
3. Run all cells to preprocess data, train models, and generate predictions  

---

## 📌 Conclusion
This project demonstrates:
- Handling missing values effectively  
- Feature engineering for improved learning  
- Training & comparing multiple ML models  
- Hyperparameter tuning & threshold optimization for best results  

---
