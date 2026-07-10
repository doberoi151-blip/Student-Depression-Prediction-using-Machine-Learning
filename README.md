# Student Depression Prediction Using Machine Learning

## Project Overview

This project aims to predict whether a student is likely to experience depression based on various demographic, academic, and behavioral factors. The project follows a complete machine learning workflow, including data preprocessing, feature engineering, model training, and performance evaluation.

---

## Problem Statement

Mental health is an important aspect of student well-being. The goal of this project is to build a machine learning model that can identify potential depression cases using student-related data.

---

## Dataset Information

The dataset contains information related to students, including:

- Gender
- Academic Performance
- Stress Level
- Anxiety Level
- Addiction Level
- Platform Usage
- Other behavioral and demographic features

### Target Variable

- `depression_label`
  - 0 = Not Depressed
  - 1 = Depressed

---

## Data Preprocessing

The following preprocessing steps were performed:

### 1. Data Cleaning
- Loaded dataset using Pandas
- Checked dataset shape and information
- Verified data types

### 2. Missing Value Handling
- Checked missing values using:

```python
df.isnull().sum()
```

### 3. Duplicate Removal

```python
df.drop_duplicates()
```

### 4. Categorical Encoding

#### Label Encoding
Applied on binary categorical columns such as Gender.

#### One-Hot Encoding
Applied on:

```python
platform_usage
```

using:

```python
OneHotEncoder()
```

---

## Feature Engineering

- Encoded categorical variables
- Combined encoded features with the original dataset
- Removed unnecessary categorical columns after encoding

---

## Train-Test Split

Dataset was divided into:

```python
80% Training Data
20% Testing Data
```

using:

```python
train_test_split()
```

---

## Model Training

A classification model was trained to predict depression status.

Example:

```python
model.fit(X_train, y_train)
```

---

## Model Evaluation

### Accuracy

```text
Train Accuracy = 98.85%
Test Accuracy = 99.16%
```

### Confusion Matrix

```text
[[234   0]
 [  2   4]]
```

### Classification Report

| Metric | Class 1 |
|----------|----------|
| Precision | 1.00 |
| Recall | 0.67 |
| F1 Score | 0.80 |

---

## Key Findings

- The model achieved high accuracy on unseen test data.
- The dataset is highly imbalanced:
  
```text
Class 0 = 1169
Class 1 = 31
```

- Despite class imbalance, the model successfully detected most depression cases.
- Recall can be further improved using imbalance handling techniques.

---

## Libraries Used

```python
pandas
numpy
matplotlib
seaborn
scikit-learn
```

---

## Project Workflow

```text
Data Collection
      ↓
Data Cleaning
      ↓
EDA
      ↓
Encoding
      ↓
Feature Engineering
      ↓
Train-Test Split
      ↓
Model Training
      ↓
Prediction
      ↓
Evaluation
```

---

## Future Improvements

- Apply SMOTE for class imbalance handling
- Compare multiple models:
  - Logistic Regression
  - Decision Tree

---

## Author

Dev Srivastava

B.Tech CSE Student

Interested in Machine Learning, Data Science, AI/ML, and Software Development.

---

## Technologies

Python • Pandas • NumPy • Scikit-Learn • Jupyter Notebook • Machine Learning
