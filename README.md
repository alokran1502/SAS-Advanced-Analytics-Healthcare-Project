# SAS-Advanced-Analytics-Healthcare-Project
U.S. Hospital Patient Experience &amp; Service Issue Analysis
# Mental Health in the Tech Industry Analysis using SAS

## 📌 Project Overview
This project addresses a critical corporate business scenario: analyzing employee mental health, workplace support systems, and the underlying factors that influence tech professionals to seek mental health treatment. 

Acting as a **Data Analyst** for a multinational technology corporation, the objective of this project is to ingest, clean, and analyze employee survey data using **SAS Programming**. The final output provides evidence-based, actionable insights to the Human Resources (HR) department to optimize workplace well-being, benefits packages, and corporate mental health policies.

---

## 🛠️ Tech Stack & Tools
* **Language:** SAS (Statistical Analysis System)
* **Procedures Used:** `PROC IMPORT`, `PROC CONTENTS`, `PROC MEANS`, `PROC FREQ`, `PROC TTEST`, `PROC ANOVA`, `PROC CORR`, `PROC SQL`, `PROC REPORT`, `PROC LOGISTIC`
* **Reporting & Automation:** SAS Macro Language, ODS (Output Delivery System)
* **Documentation & Visualization:** Microsoft Excel, PDF, Markdown

---

## 📂 Project Structure & Deliverables
The project deliverables are organized into a single compressed package (`YourName_Projecttitle.zip`) containing the following essential components:

```text
├── 📜 README.md                    # Project documentation (this file)
├── 💻 code/
│   └── mental_health_analysis.sas  # Well-commented, complete SAS production code
├── 📊 data/
│   ├── raw_survey_data.csv         # Original CSV dataset received from HR
│   └── cleaned_mental_health.sas7bdat # Cleaned & transformed SAS dataset
├── 🖨️ output/
│   ├── statistical_results.pdf    # ODS exported PDF report of all procedures
│   └── management_summary.xlsx    # ODS exported Excel workbook for stakeholders
└── 💼 documentation/
    ├── Management_Report.pdf       # Comprehensive 5–8 page business insight report
    └── Executive_Presentation.pptx # 10–15 slide presentation deck for senior executives
```

---

## ⚙️ Core Tasks & Methodology

### 1. Data Ingestion & Auditing (Section 1)
* Imported raw CSV files securely via `PROC IMPORT` and verified rows using the first 20 records.
* Examined dataset metadata (`PROC CONTENTS`) to log observations, variables, data types, and discover missing values.
* Generated baseline descriptive metrics (`PROC MEANS`) targeting central tendencies and variances of numerical features.

### 2. Data Cleansing & Feature Engineering (Section 2)
* Filtered out extreme age anomalies (retaining exclusively ages 18 to 70).
* Resolved and standardized text discrepancies within the `Gender` variable.
* Formulated logical classification buckets via categorical engineering:
  * **`Age_Group`:** 18–25, 26–35, 36–45, and 46+.
  * **Flags (0/1):** Generated binary flags for `Treatment_Flag`, `Remote_Work_Flag`, and `Family_History_Flag`.

### 3. Exploratory Data Analysis & SQL Reporting (Sections 3 & 5)
* Evaluated demographic breakdowns and geographical densities via descriptive cross-tabulations (`PROC FREQ`).
* Leveraged standard `PROC SQL` queries to evaluate global distributions, discovering treatment-seeking rates, mean age distributions, and extreme variations across international offices.

### 4. Advanced Statistical Modeling (Section 4 & Bonus)
To remove corporate guesswork, hypothesis testing was applied to reveal what truly drives care-seeking trends:
* **Chi-Square Tests:** Evaluated dependencies between treatment-seeking habits and variables like gender, family history, and workplace care options.
* **Independent T-Tests & ANOVA:** Evaluated variations in average age against clinical treatment choices and workplace productivity interference tiers.
* **Logistic Regression (`PROC LOGISTIC`):** Constructed a predictive model evaluating the odds ratios of variables like remote work, company benefits, and work interference on an employee's choice to pursue mental health services.

### 5. SAS Macro Automation (Section 6)
Engineered reusable macro programs to automate complex reporting sequences dynamically:
* `%CountryReport(country)`: Dynamically builds customized demographic metrics for any specified region.
* `%MentalHealthAnalysis(variable)`: Standardizes the pipeline for variable frequency distribution, cross-tabulations, and automatic Chi-Square generation.
* Dynamic looping scripts that autonomously compile and separate distinct localized metrics per country without hardcoded commands.

---

## 📈 Key Insights & Recommendations Summary
*(Note: Fill these in with your specific data outcomes after running your code)*
* **Workplace Triggers:** Identified the statistical relationship between `Work Interference` metrics and employee retention/well-being.
* **Demographic Target:** Determined exactly which `Age_Group` is most vulnerable and highly likely to request treatment.
* **Actionable Corporate Directives:** Outlined 5 clear organizational modifications for HR—ranging from optimized benefit distribution to localized leadership coaching plans.

---

## 🚀 How to Run the Program

1. Open your **SAS Studio** or **SAS Enterprise Guide** environment.
2. Clone this repository or download the `.sas` file from the `code/` folder.
3. Upload the raw dataset (`raw_survey_data.csv`) to your designated SAS directory environment.
4. Modify the `FILENAME` or library path references at the top of the script to match your native directory structure:
   ```sas
   LIBNAME techmh '/your-secure-sas-path/data';
   ```
5. Run the script sequentially to generate all datasets, statistical matrices, and macro configurations.
6. Check your designated output folder for the generated `.xlsx` and `.pdf` presentation summaries.

---

## 📜 Academic/Corporate Disclaimer
This project was developed under realistic corporate parameters to satisfy data-driven enterprise HR metrics. It contains analytical calculations, automation modules, and programmatic components optimized for rigorous organizational review.
