# 🔬 Predicting Raw Material Quality in Manufacturing

This project focuses on building statistical models to understand and predict the **quality of raw materials** in a manufacturing process. The goal is to identify which process parameters most influence quality outcomes and to build models that support early quality classification and decision-making.

---

## 🎯 Objective

- Analyze the impact of chamber temperatures, layer height, and material humidity on material quality
- Build multiple **linear regression models** to predict continuous quality scores
- Build **logistic regression models** to classify whether a batch meets the required quality threshold
- Interpret model outputs and extract actionable insights for process optimization

---

## 📂 Repository Contents

| File Name                   | Description                                |
|----------------------------|--------------------------------------------|
| `README.md`                | This documentation file                    |
| `Project_Report.pdf`       | Detailed analysis, model results, and insights |
| `Manufacturing_Data.xlsx`  | Dataset with sensor readings *(confidential; not included)*

> ⚠️ **Note:** The dataset used in this project is proprietary and **not included** in this repository.

---

## 📉 Linear Regression Models

A total of **9 linear regression models** were built to estimate the numeric quality score based on different sets of process parameters.

| Model | Variables Used                                 | R² Score | Notes                                           |
|-------|------------------------------------------------|----------|-------------------------------------------------|
| 1     | Chamber 1 sensors (3 values)                   | 0.032    | Not significant                                 |
| 2     | Chamber 2 sensors                              | 0.011    | Not significant                                 |
| 3     | Chamber 3 sensors                              | **0.634** | Strong fit; **Chamber 3 has negative impact**   |
| 4     | Chamber 4 sensors                              | 0.0004   | Not significant                                 |
| 5     | Chamber 5 sensors                              | 0.047    | Weak significance                               |
| 6     | Average temperature from all chambers          | 0.720    | Strong base model                               |
| 7     | Model 6 + Layer Height                         | **0.747** | Layer height significant, improves model        |
| 8     | Model 7 + Material Humidity                    | **0.747** | Humidity **not significant**                    |
| 9     | Model 8 + Layer Height Squared                 | **0.747** | Squared term **not significant**, coef negative |

---

## 🧮 Logistic Regression Models

Logistic models were used to classify whether batches met a **quality threshold of ≥ 400**.

| Model | Variables Used                                   | Accuracy | Pseudo R² | Notes                                          |
|-------|--------------------------------------------------|----------|------------|------------------------------------------------|
| 10    | Average chamber temperatures                     | 88.34%   | 0.706      | Chamber 3 negative; others positive            |
| 11    | Model 10 + Layer Height + Material Humidity      | **89.75%** | **0.730**    | Layer height improved performance; humidity not significant |

---

## 🔍 Key Insights

- **Chambers 1, 2, and 5**: Positive effect on quality
- **Chamber 3**: Consistently negative impact
- **Layer height**: Important predictor with potential non-linear behavior
- **Material humidity**: Not statistically significant in the dataset
- **Up to 89.75% classification accuracy** achieved using logistic regression

---

## 📁 Repository URL

> GitHub Repository: [https://github.com/yourusername/manufacturing-quality-prediction]([https://github.com/yourusername/manufacturing-quality-prediction](https://github.com/moni0811/Linear-and-Logistic-Regression-using-Excel.git))

---

## 👤 Author

**Monisha S**  
Data Professional – Predictive Analytics & Manufacturing Optimization  
📧 you@example.com

---

## 📃 Disclaimer

The dataset used in this project is **confidential** and has not been included in this repository. Results and models are for internal demonstration and evaluation purposes only.
