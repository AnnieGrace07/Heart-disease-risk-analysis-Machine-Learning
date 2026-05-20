# Heart-disease-risk-analysis using K-Means Clustering and Association Rule Mining
## 📌 Project Overview

Cardiovascular diseases (CVDs) are the leading cause of death globally, accounting for nearly 17.9 million deaths annually.

This project analyzes heart disease-related data using **unsupervised machine learning techniques** to discover meaningful patient patterns and identify possible risk factors associated with heart disease.

The analysis focuses on:

- **K-Means Clustering**
- **Association Rule Mining (Apriori Algorithm)**

The goal was to explore relationships between medical indicators and uncover hidden patterns in heart disease data.

---
**Source:** Kaggle

The dataset contains medical information used for heart disease prediction.

### Dataset Characteristics
- **918 observations (rows)**
- **12 variables (columns)**
- No missing value imputation required
- Mix of:
  - Numerical variables
  - Categorical variables

### Variables Included
- Age
- Sex
- Cholesterol
- Blood Pressure
- Maximum Heart Rate
- Resting ECG
- Chest Pain Type
- Fasting Blood Sugar
- Heart Disease Indicator

---

## 🔗 Python Code

Google Colab Notebook:

[Open Colab Notebook](https://colab.research.google.com/drive/105znJq6gpksj_3q0Eo3hbok-xIdQHvoz?usp=sharing)

---

## 🎯 Project Objectives

### 1. K-Means Clustering
To identify hidden patient groups based on medical features such as:

- Age
- Cholesterol
- Maximum Heart Rate
- Other clinical indicators

The objective was to determine whether clusters aligned with known medical physiology patterns.

### 2. Association Rule Mining
To identify **if-then relationships** between medical conditions and heart disease indicators.

The goal was to uncover hidden associations that may support clinical investigation.

---

## 🧠 Machine Learning Techniques Used

### 1️⃣ K-Means Clustering

K-Means clustering was applied to identify patient groups without using labeled outcomes.

### Process:
- Feature scaling performed
- Elbow Method used to determine optimal K
- Clusters analyzed based on physiology trends

### Key Findings
✔️ **2 clusters** showed meaningful physiological patterns:

**Cluster 1**
- Younger individuals
- Higher maximum heart rate

**Cluster 2**
- Older individuals
- Lower maximum heart rate

When **K = 3**, clusters provided clearer risk distinctions:

- Low Risk
- Moderate Risk
- High Risk

### Important Observation
As age increases, maximum heart rate generally declines — matching known human physiology.

---

### 2️⃣ Association Rule Mining

The **Apriori Algorithm** was applied to identify strong medical relationships.

### Variables Selected
- Sex
- Chest Pain Type
- Fasting Blood Sugar
- Heart Disease Indicator

Categorical variables were transformed using:

```python
get_dummies()
```

### Key Findings
At **support = 0.5**, no meaningful rules were found.

After reducing support to **0.3**, meaningful associations emerged.

#### Example Rule:
**If chest pain is asymptomatic → Higher probability of heart disease**

Key insight:
- **79% of asymptomatic chest pain patients were more likely to have heart disease**
- Applies to **42.7% of total dataset**

---

## 📊 Results Summary

| Technique | Outcome |
|------------|----------|
| K-Means Clustering | Patient segmentation into meaningful risk groups |
| Association Rule Mining | Hidden medical condition relationships identified |

---

## 📈 Key Insights

✔️ Maximum heart rate declines with age  
✔️ Clustering aligned with known medical physiology  
✔️ Risk profiling improves when more variables are included  
✔️ Association rule mining uncovered hidden medical relationships  
✔️ Asymptomatic chest pain showed strong correlation with heart disease risk

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-Learn
- mlxtend (Apriori)
- Matplotlib
- Google Colab
- Machine Learning

---

## 🚀 Future Improvements

- Add supervised learning models
- Compare clustering techniques
- Expand medical variables
- Improve association rule tuning
- Add predictive heart disease classification

---

## 💡 Key Learning

This project strengthened my understanding of:

- Unsupervised Machine Learning
- Clustering Analysis
- Pattern Discovery
- Healthcare Analytics
- Data Interpretation
- Feature Relationships
