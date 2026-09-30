# Final Project Summary
This project takes a deep dive into the Titanic dataset to understand what really drove passenger survival. I built a clean data pipeline to handle missing details—like filling in ages based on passenger titles—and ran an exploratory analysis across key factors like gender, class, and family size. The findings show clear patterns around priority boarding, upper-deck access, and family mobility during the evacuation. To pull it all together, I created an interactive dashboard that translates these historical trends into practical insights for emergency planning and resource management.

# 🚢 Titanic Survival Analysis & Demographic Insights

An end-to-end data analytics project exploring passenger survival patterns on the RMS Titanic. This project includes structured data cleaning, domain-aware missing value imputation, exploratory data analysis (EDA), interactive dashboard visualization, and operational safety insights.

---

## 📌 Project Overview

On April 15, 1912, the RMS Titanic sank after colliding with an iceberg, leading to the loss of 1,502 lives out of 2,224 passengers and crew. This project analyzes **891 passenger records** to identify the primary demographic and socioeconomic drivers of survival.

### Core Objectives
1. **Data Pipeline Integrity:** Handle missing values (`Age`, `Embarked`, `Cabin`), standardize data types, and engineer domain-specific features.
2. **Exploratory Data Analysis (EDA):** Quantify survival variance across gender, age cohorts, ticket class (`Pclass`), and family structure (`SibSp`, `Parch`).
3. **Visual Intelligence:** Build interactive visualizations using Python (`Plotly` / `Seaborn`) for dynamic filtering and trend analysis.
4. **Key Insights:** Translate historical data patterns into actionable emergency management and resource allocation lessons.

---

## 📊 Repository Structure

```text
├── data/
│   ├── raw_titanic.csv               # Original 891-record training set
│   └── cleaned_titanic.csv             # Processed dataset with engineered features
├── notebooks/
│   ├── 01_data_cleaning.ipynb         # Missing value imputation & feature engineering
│   └── 02_exploratory_data_analysis.ipynb # Statistical EDA & visualizations
├── dashboard/
│   ├── app.py                         # Plotly/Dash interactive dashboard code
│   └── dashboard_preview.png          # Visual layout screenshot
├── reports/
│   ├── Titanic_Survival_Analysis_Final_Project.docx # Formatted MS Word Report
│   └── Titanic_Survival_Analysis_Final_Project.pdf  # PDF Export
└── README.md                          # Project documentation

---

🛠️ Data Cleaning & Feature Engineering

Age Imputation: Grouped median imputation by Pclass and extracted passenger titles (Mr, Mrs, Miss, Master).

Embarked Imputation: Mode imputation using 'S' (Southampton) for 2 missing records.

Cabin Transformation: Created binary indicator Has_Cabin (1 if recorded, 0 otherwise) due to high missingness (77.1%).

Family Size Construction: Engineered FamilySize = SibSp + Parch + 1 and created a boolean flag Is_Alone.

📄 Final Project Deliverable

The complete, professionally styled report is available in Microsoft Word (.docx) format inside the folder.
