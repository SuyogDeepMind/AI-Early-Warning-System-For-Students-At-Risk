# AI Early Warning System for Students at Risk

> *Using Machine Learning to Predict and Prevent Academic Failure Before It Happens.*

---

## 🧠 Project Overview

This project presents an AI-powered Early Warning System designed to identify students at risk of academic failure using machine learning models. By analyzing a range of academic, behavioral, and social features, the system aims to predict whether a student will pass or fail — enabling timely interventions by educators.

## 🎯 Objective

To build a predictive system using supervised machine learning models that:

* Forecasts student academic success based on historical data
* Identifies key features contributing to student performance
* Enables early intervention to prevent failure

---

## 📂 Dataset

* **Source**: UCI Machine Learning Repository - [Student Performance Dataset](https://archive.ics.uci.edu/ml/datasets/student+performance)
* **Focus**: `student-mat.csv` (Math subject data only)
* **Size**: 395 records, 33 features

### 🎓 Target Variable

* `G3` - Final grade
* Transformed into binary `pass` (1 if G3 >= 10 else 0)

### 🧾 Key Features Used

* Demographic: `sex`, `age`, `address`, `famsize`, etc.
* Academic: `studytime`, `failures`, `absences`, etc.
* Social: `romantic`, `goout`, `health`, etc.

---

## 🧪 Preprocessing Steps

### 🔹 Handling Missing Values

* No missing values found in the dataset.

### 🔹 Encoding Categorical Features

* Used **Label Encoding** on categorical columns such as `school`, `sex`, `address`, etc.

### 🔹 Feature Scaling

* Applied **StandardScaler** to all numeric features except the target to normalize distributions and improve model performance.

### 🔹 Avoiding Data Leakage

* Dropped intermediate grade columns `G1` and `G2` which were highly correlated with `G3` to ensure realistic evaluation.

---

## 🔍 Exploratory Data Analysis

* Visualized distribution of the `pass` label.
* Used heatmaps to inspect feature correlations.
* Found high correlation between past grades and final result.
* Observed socio-academic behavior patterns in successful students.

---

## 🤖 ML Models & Hyperparameter Tuning

Used **GridSearchCV** for hyperparameter tuning and selected models based on accuracy and performance metrics:

### Algorithms Tried:

* Logistic Regression
* Support Vector Classifier (SVC)
* Decision Tree
* Random Forest
* Gradient Boosting
* XGBoost *(optional if system supports)*

### Evaluation Metrics:

* Accuracy Score
* Classification Report
* Confusion Matrix

---

## ✅ Best Model Summary

* **Model**: Random Forest / XGBoost *(based on system performance)*
* **Accuracy Achieved**: \~96%
* **Key Insight**: Study time, failures, absences, and social factors like going out and romantic relationship status significantly impact academic performance.

---

## 💡 Real-World Applications

* **Schools/Colleges**: Alert system for teachers to flag at-risk students
* **EdTech Startups**: Adaptive learning platforms to provide remedial content
* **Policymakers**: Tailored support strategies based on data-driven insights

---

## 🚀 How to Run the Notebook

1. Clone the repository
2. Install dependencies using `requirements.txt`
3. Run the Jupyter Notebook `student_performance.ipynb`
4. Review final model performance and visual insights

---

## 📁 Project Structure

```
AI_Early_Warning_Student_Risk/
├── student-mat.csv
├── student_performance.ipynb
├── README.md
└── requirements.txt
```

---

## 🛠️ Tech Stack

* Python
* Pandas, NumPy, Matplotlib, Seaborn
* scikit-learn
* XGBoost *(optional)*

---

## 🙌 Author

**Suyog Manke**
Data Science & AI Enthusiast
Passionate about solving real-world problems using ML and AI.

---

## 📌 Note

If you're using a Mac and facing issues with XGBoost, ensure OpenMP is installed:

```
brew install libomp
```

---

👨‍💻 Author
Suyog Manke
Powered with ❤️ by Suyog Manke

## 📫 Connect With Me

[LinkedIn](#) | [GitHub](#) | [Email](#)

---

> “The goal is not just prediction — it’s timely intervention that changes outcomes.”
