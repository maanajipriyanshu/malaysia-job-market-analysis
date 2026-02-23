# 🇲🇾 Malaysia Job Market Analysis 2024

A complete end-to-end data analysis project exploring hiring trends, salary benchmarks, and in-demand roles across Malaysia using **69,024 real job postings** from JobStreet Malaysia.

---

## 📊 Dashboard Preview

> Built with Power BI — interactive dashboard with slicers for Industry and Location filtering.

![Dashboard Preview](dashboard/Malaysia_Job_Market_Analysis_2024.pdf)

---

## 🔍 Key Insights

- 📍 **Penang pays 32% more** than the national average (RM 7,216 vs RM 5,468 in KL) — despite having fewer job postings
- 💻 **ICT is the #3 highest paying industry** (RM 6,422/month avg) and #3 in demand with 8,675 job postings
- 🏦 **Accounting has the most jobs** (11,308) but only ranks #13 in salary — high competition, average pay
- 👔 **90% of Malaysian jobs are Full Time** — strong market stability for international job seekers
- 🔧 **Network Engineering** is the highest paying ICT role at RM 13,358/month — but only 20 openings
- 📈 **Business/Systems Analysts** average RM 6,108/month with 182 openings — best balance of pay and demand for data professionals

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| Python (Pandas, NumPy, Regex) | Data cleaning, EDA |
| SQL (SQLite) | Analytical queries with CTEs and window functions |
| Power BI | Interactive dashboard |
| Git & GitHub | Version control |
| Jupyter Notebook | Reproducible analysis workflow |

---

## 📁 Project Structure

```
malaysia-job-market-analysis/
│
├── data/
│   ├── jobstreet_cleaned.csv        # 69,024 cleaned job postings
│   └── jobstreet_companies.csv      # Filtered real employers only
│
├── notebooks/
│   ├── 01_first_look.ipynb          # Data cleaning & EDA
│   └── 02_sql_analysis.ipynb        # SQL queries & insights
│
├── dashboard/
│   ├── Malaysia_Job_Market_Analysis_2024.pbix   # Power BI file
│   └── Malaysia_Job_Market_Analysis_2024.pdf    # Dashboard export
│
└── README.md
```

---

## 🔄 Methodology

### 1. Data Collection
- Source: [JobStreet All Job Dataset](https://www.kaggle.com/datasets/azraimohamad/jobstreet-all-job-dataset) via Kaggle
- 69,024 job postings from JobStreet Malaysia (2024)
- 11 raw columns including job title, company, location, category, salary, and listing date

### 2. Data Cleaning (Python)
- Standardized `job_type` column — consolidated 11 variations into 4 clean categories
- Extracted numeric salary values from text strings using Regex (e.g. "RM 2,800 – RM 3,200 per month" → min: 2800, max: 3200, avg: 3000)
- Parsed listing dates and extracted month for time-based analysis
- Removed recruitment agencies from company analysis to show real employer demand
- Handled 37,430 missing salary values (54% of dataset) — identified as a market insight itself

### 3. SQL Analysis
- Loaded cleaned data into SQLite database
- Wrote 3 analytical queries using CTEs and RANK() window functions:
  - Salary and demand ranking by industry
  - Salary ranking by location (min 200 job postings)
  - ICT subcategory salary breakdown

### 4. Dashboard (Power BI)
- 4 KPI cards: Total postings, Avg salary, Unique companies, Industries
- 5 interactive visuals with Industry and Location slicers
- Dark professional theme with average line annotations

---

## 💡 Why This Project

As a data professional targeting the Malaysian job market, I wanted to go beyond generic salary surveys and analyze real, current hiring data. This project answers questions any job seeker or HR professional in Malaysia would actually care about:

- Which industries pay the most?
- Which cities should I target?
- What ICT role gives the best balance of pay and opportunity?
- How transparent are Malaysian employers about salary?

---

## 👤 About Me

**Priyanshu Singh** — Data Analyst  
📧 maanapriyanshu@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/maanapriyanshurajput)

---

*Dataset source: JobStreet Malaysia job postings via Kaggle. Analysis conducted for portfolio purposes.*
