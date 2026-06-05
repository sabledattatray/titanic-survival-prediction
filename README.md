# 🚢 Titanic Survival Prediction

A Machine Learning project built using Python and Scikit-learn to predict passenger survival on the Titanic dataset from Kaggle.

![Titanic Project](https://raw.githubusercontent.com/sabledattatray/titanic-survival-prediction/main/Kagel%20Image%20Jun%206%2C%202026%2C%2002_45_26%20AM.png)

## 📌 Project Overview

The goal of this project is to predict whether a passenger survived the Titanic disaster using demographic and travel-related information such as age, gender, passenger class, fare, and family size.

This project demonstrates the complete Machine Learning workflow:

- Data Loading
- Data Cleaning
- Missing Value Handling
- Feature Engineering
- Model Training
- Model Evaluation
- Kaggle Submission

---

## 🎯 Objective

Predict whether a passenger survived the Titanic shipwreck.

Target Variable:

| Value | Meaning |
|---------|---------|
| 0 | Did Not Survive |
| 1 | Survived |

---

## 📊 Dataset

Source:
https://www.kaggle.com/competitions/titanic

Files Used:

- train.csv
- test.csv
- gender_submission.csv

Training Dataset:

- 891 passengers
- 12 features

Test Dataset:

- 418 passengers

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Jupyter Notebook

---

## 🔍 Data Preprocessing

### Missing Values

Handled missing values using:

- Age → Median
- Fare → Median
- Embarked → Most frequent value (S)

### Removed Columns

Dropped:

- Cabin

Reason:
More than 77% of values were missing.

---

## ⚙️ Feature Engineering

### Original Features

- Pclass
- Sex
- Age
- SibSp
- Parch
- Fare

### Additional Features

#### FamilySize

```python
FamilySize = SibSp + Parch + 1
```

#### Embarked Encoding

```python
S = 0
C = 1
Q = 2
```

#### Sex Encoding

```python
Male = 0
Female = 1
```

---

## 🤖 Machine Learning Model

Algorithm:

### Random Forest Classifier

```python
RandomForestClassifier(
    n_estimators=200,
    random_state=42,
    max_depth=5,
    min_samples_split=10,
    min_samples_leaf=5
)
```

---

## 📈 Model Evaluation

### Validation Accuracy

| Model | Accuracy |
|---------|---------|
| Model v1 | 0.8045 |
| Model v2 | 0.7989 |
| Model v3 | 0.8101 |

Best Validation Accuracy:

```text
81.01%
```

---

## 🏆 Kaggle Results

### Submission 1

Score:

```text
0.73205
```

### Submission 2

Score:

```text
0.78229
```

Improvement:

```text
+0.05024
```

---

## 📂 Project Structure

```text
Titanic/
│
├── train.csv
├── test.csv
├── gender_submission.csv
│
├── Titanic_Survival_Prediction.ipynb
│
├── submission.csv
├── submission_v2.csv
│
├── README.md
│
└── images/
    └── titanic-banner.png
```

---

## 📸 Project Workflow

1. Load Dataset
2. Explore Data
3. Handle Missing Values
4. Encode Categorical Features
5. Create FamilySize Feature
6. Train Random Forest Model
7. Evaluate Using Validation Set
8. Generate Predictions
9. Submit to Kaggle
10. Analyze Results

---

## 🚀 Key Learnings

- Data Cleaning
- Feature Engineering
- Model Validation
- Classification Problems
- Random Forest Models
- Kaggle Competition Workflow
- Machine Learning Project Development

---

## 🔮 Future Improvements

- Extract passenger titles (Mr, Mrs, Miss, Master)
- Hyperparameter tuning
- Cross-validation
- XGBoost
- LightGBM
- Feature importance analysis

---

## 👨‍💻 Author

**Datta Sable**

- LinkedIn: https://linkedin.com/in/dattasable
- Portfolio: https://dattasable.com

---

### ⭐ If you found this project useful, consider starring the repository.
