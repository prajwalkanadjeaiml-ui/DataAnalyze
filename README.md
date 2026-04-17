# DataAnalyze

# 📊 College Admissions & Institutional Performance Analysis

> **Data Analytics Mini Project** | BTech Computer Engineering | G H Raisoni Skill Tech University, Pune

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Google_Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

---

## 🧠 Problem Statement

I am analyzing a dataset of **777 US colleges** to understand what institutional factors—such as application acceptance rates, faculty qualifications, expenditure per student, and student-to-faculty ratios—influence graduation rates. This analysis can help educational policymakers and prospective students identify which college characteristics are most strongly associated with student success and institutional quality.

---

## 📁 Dataset Description

| Property | Details |
|---|---|
| **Dataset Name** | US College Dataset |
| **Source** | ISLR R Package / Kaggle |
| **Rows** | 777 |
| **Columns** | 19 |
| **File** | `College.csv` |

### 📋 Column Reference

| Column | Type | Description |
|---|---|---|
| `College` | Categorical | Name of the college |
| `Private` | Categorical | Private institution? (Yes / No) |
| `Apps` | Numeric | Number of applications received |
| `Accept` | Numeric | Number of applications accepted |
| `Enroll` | Numeric | Number of new students enrolled |
| `Top10perc` | Numeric | % of new students from top 10% of HS class |
| `Top25perc` | Numeric | % of new students from top 25% of HS class |
| `F.Undergrad` | Numeric | Full-time undergraduates |
| `P.Undergrad` | Numeric | Part-time undergraduates |
| `Outstate` | Numeric | Out-of-state tuition ($) |
| `Room.Board` | Numeric | Room & board cost ($) |
| `Books` | Numeric | Estimated book cost ($) |
| `Personal` | Numeric | Estimated personal spending ($) |
| `PhD` | Numeric | % of faculty with PhD |
| `Terminal` | Numeric | % of faculty with terminal degree |
| `S.F.Ratio` | Numeric | Student-to-faculty ratio |
| `perc.alumni` | Numeric | % of alumni who donate |
| `Expend` | Numeric | Instructional expenditure per student ($) |
| `Grad.Rate` | Numeric | Graduation rate (%) — **Target Variable** |

---

## 🗂️ Project Structure

```
📦 college-data-analytics
 ┣ 📓 College_Data_Analytics.ipynb   ← Main Colab Notebook
 ┣ 📄 College.csv                    ← Dataset
 ┗ 📄 README.md                      ← This file
```

---

## 🔬 What's Inside the Notebook

### 1️⃣ Problem Statement & Dataset Description
- Goal defined clearly
- Column-by-column breakdown

### 2️⃣ Library Imports
```python
pandas, numpy, matplotlib, seaborn, scipy, sklearn
```
All imported in a single cell.

### 3️⃣ Data Cleaning & Statistics
- Loaded dataset, displayed first 5 rows, shape, dtypes
- Checked and handled **missing values** (none found — documented)
- Removed **duplicate rows** (none found — documented)
- Calculated for `Grad.Rate` and `Outstate`:
  - Mean, Median, Mode, Standard Deviation, Variance, Range, Mid-range

### 4️⃣ Visualizations

| # | Chart Type | Column(s) | Insight |
|---|---|---|---|
| 1 | Histogram | `Grad.Rate` | Distribution of graduation rates across colleges |
| 2 | Count Plot | `Private` | Private (565) vs Public (212) college breakdown |
| 3 | Boxplot | `Outstate` by `Private` | Tuition spread & outliers by college type |
| 4 | Correlation Heatmap | All numeric columns | Feature relationships, especially with `Grad.Rate` |

> Every chart has a **title**, **labeled axes**, and a **markdown interpretation**.

### 5️⃣ Simple Prediction (Linear Regression)
- **Target:** `Grad.Rate`
- **Features:** `Outstate`, `Room.Board`, `Expend`, `perc.alumni`, `Top10perc`, `S.F.Ratio`, `Private` (encoded)
- **Encoding:** `LabelEncoder` on `Private` column
- **Split:** 80% Train / 20% Test
- **Metrics:** MSE, RMSE, R² Score
- **Visual:** Actual vs Predicted scatter plot

### 6️⃣ Insights & Recommendations

**Finding 1 —** Out-of-state tuition has the highest correlation (0.57) with graduation rate, suggesting better-funded colleges produce stronger outcomes.

**Finding 2 —** Private colleges charge nearly double the tuition of public ones, with a median ~$13,000 vs ~$7,000 for public institutions.

**Finding 3 —** A small cluster of colleges falls below 20% graduation rate — a significant underperforming minority vs the bulk (55–80%).

**Recommendation 1 —** Governments should increase per-student funding for underfunded public colleges; even modest investment shows measurable graduation improvement.

**Recommendation 2 —** Students should prioritize student-to-faculty ratio and PhD faculty percentage over tuition alone when choosing a college.

---

## ▶️ How to Run

1. Open [Google Colab](https://colab.research.google.com)
2. Go to **File → Upload Notebook** → upload `College_Data_Analytics.ipynb`
3. In the **Files panel** (left sidebar), upload `College.csv`
4. Click **Runtime → Run All**
5. Notebook runs top to bottom without errors ✅

---

## 🛠️ Tech Stack

- **Language:** Python 3.10+
- **Environment:** Google Colab
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, SciPy

---

## 👤 Author

**Vedant (Vedu)**  
BTech Computer Engineering — 2nd Year  
G H Raisoni Skill Tech University, Pune  

---

## 📜 License

This project is for academic purposes only.
