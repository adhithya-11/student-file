# 🎓 Student Performance Prediction

## 🎯 Objective
To analyze academic data of students and build a machine learning model to predict their final exam scores (G3). This helps in identifying students at risk and factors influencing academic performance.

---

## 📊 1. Data Preprocessing

### 🔹 Dataset Used
- **Source**: [UCI Machine Learning Repository – Student Performance Dataset](https://archive.ics.uci.edu/ml/machine-learning-databases/00320/student.zip)
- **Size**: 395 records, 33 features
- **Target Variable**: `G3` (Final Grade)

### 🔹 Steps Followed
- Checked for **missing values** (none found)
- Applied **Label Encoding** for binary categorical columns
- Applied **One-Hot Encoding** for nominal categorical columns (e.g., `school`, `address`)
- Removed features like `G1`, `G2` to avoid **data leakage**

---

## 📈 2. Exploratory Data Analysis (EDA)

- Visualized data distributions and patterns using **Matplotlib** and **Seaborn**
- Key insights:
  - Students with higher `studytime` tend to score better
  - More `failures` significantly reduce final grade
  - `absences` have moderate negative impact

---

## 🧠 3. Model Building

### ✅ Models Implemented
- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- KNN
_ SVR

### 🔍 Hyperparameter Tuning
- Used **GridSearchCV** for Decision Tree & Random Forest
- Applied **5-fold Cross-Validation** for better generalization

---

## 📊 4. Model Evaluation

### 📐 Metrics Used
- R² Score
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)

| Model              | R²        | MAE       | RMSE     |
|--------------------|-----------|-----------|----------|
| Random Forest      | 0.814791  | 1.164557  | 1.948773 |
| SVR                | 0.802993  | 1.195317  | 2.009886 |
| Linear Regression  | 0.724134  | 1.646666  | 2.378370 |
| KNN Regressor      | 0.706292  | 1.535865  | 2.454079 |
| Decision Tree      | 0.703131  | 1.357218  | 2.467248 |

✅ **Random Forest** outperformed the others and was selected for deployment.

---

## 🔍 Feature Importance (from Random Forest)

Top contributing features to `G3`:
- `failures`
- `studytime`
- `absences`
- `goout`
- `schoolsup`

---

## 🚀 5. Streamlit App Deployment

- Built an interactive frontend using **Streamlit**
- Hosted on **Streamlit Cloud**

🌐 **Live App**: [Click to Open](https://student-file-fjtepuve6y8tvtemtshtsp.streamlit.app/)

---

## 📁 Project Structure

