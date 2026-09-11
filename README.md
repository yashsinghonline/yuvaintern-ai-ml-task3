
# 📊 Telco Customer Churn Analysis

An end-to-end data analysis and exploratory research project investigating customer turnover patterns in the telecommunications industry. This repository covers data cleaning, exploratory visual analysis, key retention insights, and actionable business strategies.

---

## 📌 Project Overview
Customer churn is a critical metric in subscription-based business models. Acquiring a new customer can cost **5 to 7 times more** than retaining an existing one. 

This project analyzes subscriber demographics, service configurations, account tenures, and contract types across **7,043 telecom customers** to identify the primary drivers of churn and propose targeted retention mechanisms.

---

## 🎯 Objectives
1. **Explore Dataset Structure:** Examine variables, distributions, data types, missing records, and relationships.
2. **Clean & Preprocess Data:** Address missing billing fields, adjust data types, remove unnecessary identifiers, and re-code binary target variables.
3. **Exploratory Data Analysis (EDA):** Use Pandas, NumPy, Seaborn, and Matplotlib to uncover correlation metrics and behavior trends.
4. **Data Visualization:** Build intuitive plots (histograms, count plots, heatmaps, scatter plots) to communicate findings.
5. **Business Insights:** Deliver actionable strategy recommendations based on quantitative evidence.

---

## 📁 Dataset Details
* **Source:** IBM Telco Customer Churn Dataset
* **Records:** 7,043 rows | 21 columns
* **Target Variable:** `Churn` (`Yes` / `No`)

### Key Variables
| Feature | Type | Description |
| :--- | :--- | :--- |
| `tenure` | Numeric | Number of months the customer has stayed with the company |
| `Contract` | Categorical | Contract term (`Month-to-month`, `One year`, `Two year`) |
| `MonthlyCharges` | Numeric | Current amount billed to the customer per month |
| `TotalCharges` | Numeric | Total cumulative amount billed to the customer |
| `InternetService` | Categorical | Subscriber's internet network type (`DSL`, `Fiber optic`, `No`) |

---

## 🛠️ Data Cleaning & Preprocessing
* **Type Casting:** Converted `TotalCharges` from string/object to float64 to resolve hidden blank space errors.
* **Missing Value Imputation:** Imputed blank `TotalCharges` for brand-new subscribers ($0$ tenure) using the formula: `tenure × MonthlyCharges`.
* **Feature Mapping:** Created `Churn_Binary` ($1 = \text{Yes}, 0 = \text{No}$) to compute correlation matrices and segment churn rates cleanly.

---

## 📈 Key Insights & Findings
* **Contract Term Impact:** Customers on **Month-to-Month** contracts exhibit an alarming **42.7% churn rate**, compared to **11.3%** for 1-year and **2.8%** for 2-year contracts.
* **The 12-Month Hazard Zone:** Over **61% of all customer churn** occurs within the first 12 months of tenure.
* **High-Cost Risk:** High monthly charges ($70+) paired with `Fiber Optic` service show elevated churn when subscribers lack add-on support features (e.g., `OnlineSecurity` or `TechSupport`).

---

## 💡 Strategic Recommendations
1. **Contract Migration Incentives:** Offer targeted $5/month billing discounts to convert high-risk Month-to-Month accounts onto 1-Year plans.
2. **First 90-Day Onboarding:** Implement proactive customer service check-ins and free onboarding assistance to reduce early tenure drop-offs.
3. **Bundle Technical Services:** Include complimentary trials of `TechSupport` and `OnlineSecurity` for Fiber Optic packages to improve perceived service value.

---

## 🚀 How to Run the Code

### 1. Clone the Repository
```bash
git clone [https://github.com/your-username/telco-churn-analysis.git](https://github.com/your-username/telco-churn-analysis.git)
cd telco-churn-analysis

```

### 2. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn

```

### 3. Run the Script

```bash
python main.py

```

*(Note: The script automatically fetches the dataset directly from the online repository, so no manual file download is needed.)*

```
