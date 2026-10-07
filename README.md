# 🛡️ Prism Insurance – Policy & Claims Analysis Dashboard

An end-to-end data analysis project on insurance policies, premiums, and claims, built with **SQL, Python, and Power BI**. The dashboard helps business teams track revenue, coverage exposure, claim performance, and customer segments in one place.

![Dashboard Preview](images/dashboard.png)

---

## 📌 Table of Contents
- [Business Problem](#-business-problem)
- [Objectives](#-objectives)
- [Dataset](#-dataset)
- [Tools & Tech Stack](#%EF%B8%8F-tools--tech-stack)
- [Project Workflow](#-project-workflow)
- [Dashboard Overview](#-dashboard-overview)
- [Key Insights](#-key-insights)
- [Recommendations](#-recommendations)
- [Repository Structure](#-repository-structure)
- [How to Run](#%EF%B8%8F-how-to-run)
- [Author](#-author)

---

## 🎯 Business Problem
Prism Insurance Pvt. Ltd. needs a clear view of how its policies and claims are performing. Management wants to know:
- Which policy types bring the most premium?
- How many policies are active vs inactive?
- How are claims being handled (settled, rejected, pending)?
- Which customer age groups raise the highest claim amounts?

## ✅ Objectives
- Clean and prepare policy, customer, and claims data.
- Build KPIs for **Premium, Coverage, and Claim Amount**.
- Analyze claims by **status, policy type, and age group**.
- Create an interactive Power BI dashboard with filters for `PolicyNumber`, `ClaimNumber`, and `CustomerID`.

## 📂 Dataset
| Item | Details |
|---|---|
| Customers | 10,000 (5,000 Female / 5,000 Male) |
| Policies | ~10,000 (Active + Inactive) |
| Policy Types | Travel, Health, Auto, Life, Home |
| Claim Status | Settled, Rejected, Pending |
| Age Groups | Young Adults, Adult, Elder |

**Key columns:** `CustomerID`, `PolicyNumber`, `ClaimNumber`, `PolicyType`, `PremiumAmount`, `CoverageAmount`, `ClaimAmount`, `ClaimStatus`, `Active/Inactive`, `Gender`, `AgeGroup`

> 📝 *https://att-c.udemycdn.com/2024-07-27_06-58-32-305aa0ba4d15df98f4f45b4edf5c29b3/original.csv?response-content-disposition=attachment%3B+filename%3DInsuranceData.csv&Expires=1791378091&Signature=yWXbD2BO7QZKg4ym4RjT~LYhIXLF1w2toy0uhHUORQ6fRoZFSOyF0A4qkJ5FNNVE3efQV186Z9jQtfLjEwFmifywfdBwu4cOi3XHPc4LZtEja~7v5KzOiurdWc5LIJuTM0q0s-sqOpa072mKLQglf2GHkc9ub4pVnPO81-~oOS4q-eXfHBLqesafV7zIElLwiTMWGD2CaObPu056VGBIGdXrtjtC2McuSI33z1znZNvpNRx0P9PNEu8mk0YNe8dLbjANNO6~myV-yFzNcse~I08QikIB93vUmGbTl4nIJmBSBOVHYKrEysNrlSzcRdSHFl~dCaL0f9QQVFSmZoAdHQ__&Key-Pair-Id=K3MG148K9RIRF4*

## 🛠️ Tools & Tech Stack
- **SQL (MySQL / DB2)** – data extraction, joins, aggregations
- **Python (Pandas, NumPy)** – cleaning, transformation, validation
- **Power BI** – data modeling, DAX measures, dashboard
- **Excel** – quick checks and data review

## 🔄 Project Workflow
1. **Data Collection** – Load policy, customer, and claims tables.
2. **Data Cleaning** – Handle nulls, duplicates, and data types (Pandas).
3. **Feature Engineering** – Create `AgeGroup` and `Active/Inactive` flags.
4. **SQL Analysis** – Aggregate premium and claims by policy type and status.
5. **Data Modeling** – Build relationships in Power BI.
6. **DAX Measures** – Total Premium, Total Coverage, Total Claim Amount, Active %.
7. **Visualization** – Design the interactive dashboard.
8. **Insights** – Summarize findings and recommendations.

## 📊 Dashboard Overview
**KPI Cards**
| Metric | Value |
|---|---|
| Premium Amount | 5.97M |
| Coverage Amount | 600.33M |
| Claim Amount | 16.90M |

**Visuals**
- **Premium Amount by Policy Type** – bar chart
- **Active vs Inactive Policies** – donut chart
- **Number of Claims by Claim Status** – ribbon chart
- **Claim Amount by Age Group** – area line chart
- **Claim Status by Policy Type** – matrix table
- **Gender split** – card visuals
- **Slicers** – PolicyNumber, ClaimNumber, CustomerID

## 💡 Key Insights
- **Travel** is the top premium earner at **2.5M**, followed by Health (1.2M) and Auto (1.0M). Home is the lowest at 0.6M.
- **58.11%** of policies are active, while **41.89% (4.19K)** are inactive — a big retention opportunity.
- Claims by status: **Rejected 4.4K**, **Settled 3.4K**, **Pending 2.3K**. Rejected is the largest group.
- **Adults** raise the highest claim amount (**8.8M**), then Elders (6.4M), then Young Adults (1.7M).
- **Travel** has the highest claim value across Pending, Rejected, and Settled.
- The customer base is evenly split: **5,000 Female / 5,000 Male**.

## 🚀 Recommendations
- Investigate the high **rejection rate** and review the claim approval process.
- Clear the **pending claims** backlog to improve customer satisfaction.
- Run **renewal campaigns** for the 41.89% inactive policies.
- Review **Travel** pricing and fraud checks, as it has the highest claim values.
- Create targeted products for the **Adult** and **Elder** segments.

## 📁 Repository Structure
```
prism-insurance-analysis/
│
├── data/
│   ├── raw/                  # Original data files
│   └── cleaned/              # Cleaned data
├── sql/
│   └── analysis_queries.sql  # SQL queries
├── notebooks/
│   └── data_cleaning.ipynb   # Python (Pandas, NumPy)
├── powerbi/
│   └── Prism_Insurance.pbix  # Power BI file
├── images/
│   └── dashboard.png         # Dashboard screenshot
└── README.md
```

## ▶️ How to Run
1. Clone the repository
   ```bash
   git clone https://github.com/<your-username>/prism-insurance-analysis.git
   ```
2. Run the cleaning notebook in `notebooks/` (Python 3.9+, Pandas, NumPy).
3. Run the SQL scripts in `sql/` on your database.
4. Open `powerbi/Prism_Insurance.pbix` in **Power BI Desktop** and refresh the data.

## 👤 Author
**Mansoor**
Data Analytics Professional | Hyderabad, India

🔗 [LinkedIn](https://www.linkedin.com/in/mansoor-ali-khan-29773b184/?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_contact_details%3BEvA8ZWUPQo6sfzmFfgLBsQ%3D%3D) • 💻 [GitHub](https://github.com/Mansoor-rizz) • 📧 mansoorali.ma.326@gmail.com

⭐ If you found this project useful, please give it a star!

