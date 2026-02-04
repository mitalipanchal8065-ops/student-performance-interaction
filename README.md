# 📊 Student Performance Prediction using Machine Learning

## 📌 Project Overview

This project builds a supervised machine learning model to predict whether a student will **pass or fail** based on academic performance and interaction data.

The goal is to help educational institutions:

- Identify at-risk students early
- Improve intervention strategies
- Make data-driven academic decisions

---

## 🎯 Objective

To develop a classification model that accurately predicts student success using real-world data preprocessing, balancing techniques, and multiple machine learning algorithms.

---

## 📁 Dataset

The dataset contains:

- Academic performance indicators
- Student interaction metrics
- Behavioral features
- Target variable: `pass_fail`

Each row represents a single student.

---

## 🧹 Data Preprocessing

The following preprocessing steps were applied:

### ✅ Removed irrelevant columns
- `student_id` dropped (identifier only, no predictive value)

### ✅ Checked missing values & duplicates
- No major issues found

### ✅ Outlier detection
- Boxplots used for visualization
- Skewness analysis performed

### ✅ Encoding categorical data
- Label Encoding used to convert text categories into numeric form

---

## ⚖ Handling Class Imbalance

The dataset had imbalanced classes.

We applied:

**SMOTE (Synthetic Minority Oversampling Technique)**

This ensures:

- Balanced training data
- Reduced model bias
- Fairer predictions

---

## 🔀 Train-Test Split

Data split into:

- 75% Training
- 25% Testing

This allows evaluation on unseen data.

---

## 📏 Feature Scaling

We used:

**StandardScaler**

Scaling helps improve performance of models sensitive to feature magnitude.

---

## 🤖 Models Used

Multiple classification models were trained and compared:

### 1. Logistic Regression
- Baseline linear classifier
- Fast and interpretable

### 2. Decision Tree
- Non-linear model
- Captures feature interactions

### 3. Random Forest
- Ensemble model
- Reduces overfitting
- Stable performance

### 4. XGBoost
- Advanced boosting model
- High predictive power

---

## 📊 Evaluation Metrics

Models were evaluated using:

- Accuracy
- Precision
- Confusion Matrix
- Classification Report

These metrics help understand:

- Correct predictions
- False positives
- False negatives
- Class-wise performance

---

## ⭐ Feature Importance

Random Forest was used to analyze feature importance.

This reveals:

- Key predictors of student success
- Most influential academic indicators

---

## 🏆 Final Model

**Random Forest** was selected as the final model due to:

- Balanced performance
- Better generalization
- Reduced overfitting

The trained model was saved using:

```python
pickle.dump(model, open("model.pkl", "wb"))
```

This allows deployment without retraining.

---

## ✅ Conclusion

This project demonstrates a complete ML workflow:

- Data cleaning
- Preprocessing
- Handling imbalance
- Training multiple models
- Model evaluation
- Final model selection
- Model saving

The system can support early intervention and academic planning.

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Matplotlib
- Seaborn
- SMOTE (imbalanced-learn)

---

## ▶ How to Run

```bash
pip install -r requirements.txt
```

Then open:

```
ml_project.ipynb
```

Run all cells sequentially.

---

## 📌 Future Improvements

- Hyperparameter tuning
- Web deployment using Flask/Streamlit
- Real-time prediction dashboard
- Larger dataset integration

---

## 👨‍💻 Author

**Mitali Panchal**  
BBA Business Analytics Student  
Machine Learning Project
