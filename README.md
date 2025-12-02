# 📊 Customer Support Complaint Analysis – Power BI Dashboard  

A complete end-to-end Customer Support Analytics project built using **Power BI**, designed to analyze customer complaints, SLA performance, resolution efficiency, regional patterns, and customer satisfaction.  

This dashboard helps organizations identify complaint trends, optimize support operations, and improve customer experience through data-driven insights.

---

## 🚀 Project Overview  

This project analyzes customer complaints received across multiple channels (App, Phone, Email, Website, etc.).  
It focuses on:  
- Complaint volume & trends  
- SLA performance (SLA met vs violated)  
- Resolution time analysis  
- Priority-based distribution  
- Regional performance  
- Issue & sub-issue patterns  
- Customer satisfaction score analysis  
- Team performance comparison  

The dashboard provides clear KPIs and interactive visuals that help identify operational gaps and improve customer service quality.

---

## 📁 Repository Structure  

Customer-Support-Complaint-Analysis-Power-BI-Dashboard/
│
├── data/
│ └── customer_complaints_dataset.xlsx
│
├── screenshots/
│ ├── 01_dashboard_overview.png
│ ├── 02_complaint_trends.png
│ ├── 03_region_analysis.png
│ ├── 04_issue_type_breakdown.png
│ └── 05_satisfaction_metrics.png
│
├── reports/
│ ├── Customer_Complaint_Report.pdf
│ └── Customer_Complaint_Report.pbix
│
└── README.md


---

## 🗂 Dataset Description  

The dataset contains **realistic customer complaint fields**:

| Column Name | Description |
|------------|-------------|
| **TicketID** | Unique complaint/ticket identifier |
| **CustomerID** | Unique customer identifier (anonymized) |
| **CreatedDate** | Date/time the complaint was created |
| **ResolvedDate** | Date/time the complaint was resolved |
| **Status** | Current status (Open, Closed, Pending, Resolved, Escalated) |
| **IssueType** | Main issue category (Billing, Network, Service Failure, etc.) |
| **SubIssue** | More specific complaint detail |
| **Channel** | Complaint submission channel (App, Phone, Email, etc.) |
| **Priority** | Complaint priority (High, Medium, Low) |
| **ResolutionTimeHours** | Total hours taken to resolve ticket |
| **SLA_DeadlineHours** | Allowed SLA time window |
| **SLA_Compliance** | Yes/No – whether resolved within SLA |
| **SatisfactionScore** | Customer satisfaction rating (1–5) |
| **AssignedTeam** | Team handling the complaint |
| **Region** | Customer region/area |
| **PlanType** | Customer subscription plan type |
| **DeviceType** | Device used by the customer |
| **ComplaintDescription** | Text description of the issue |

---

## 🧮 Key DAX Measures  

```DAX
Total Complaints = COUNT('Dataset'[TicketID])

SLA Compliance % =
DIVIDE(
    CALCULATE(COUNTROWS('Dataset'), 'Dataset'[SLA_Compliance] = "Yes"),
    COUNTROWS('Dataset')
)

Average Resolution Time (Hours) =
AVERAGE('Dataset'[ResolutionTimeHours])

Avg Satisfaction Score =
AVERAGE('Dataset'[SatisfactionScore])

Resolution Time Variance =
VAR AvgTime = [Average Resolution Time (Hours)]
RETURN
AVERAGE('Dataset'[ResolutionTimeHours] - AvgTime)


📊 Dashboard Features
✔ Key Metrics

Total Complaints

SLA Compliance %

Avg. Resolution Time (hours)

Avg. Satisfaction Score

High Priority Complaint Ratio

✔ Complaint Analytics

Trend of complaints over time

Issue & Sub-Issue distribution

Channel performance comparison

Priority-level analysis

✔ Operational Efficiency

SLA performance analysis

Resolution time deviation

Team-wise performance

✔ Customer Experience

SatisfactionScore distribution

Relationship between SLA & Satisfaction

Issue types leading to low satisfaction

✔ Regional Insights

Complaints by Region

Region-based SLA performance

Key regional problem areas

📷 Report Screenshots
Dashboard Overview

Complaint Trends

Region Analysis

Issue Type Breakdown

Satisfaction Metrics

🧠 Key Insights

🔺 Network/Service-related issues are the highest contributors to total complaints.

⚠️ High Priority tickets show the lowest SLA compliance, indicating resource bottlenecks.

📉 SatisfactionScore drops significantly for complaints resolved beyond SLA.

🌍 Region A & Region B show consistently higher complaint volume, requiring operational improvement.

📞 App and Call Center channels receive the highest number of complaints, making them key focus areas for support optimization.

🛠 How to View the Dashboard
Option 1 — PDF Report (Quick View)

Open:
/reports/Customer_Complaint_Report.pdf

Option 2 — Interactive Power BI File (.pbix)

Requirements:

Power BI Desktop (2023 or later)

Steps:

Download the .pbix file from the reports/ folder

Open using Power BI Desktop

Interact with slicers, charts, and pages

🧑‍💻 Tech Stack

Power BI Desktop

Power Query

DAX (Data Analysis Expressions)

Excel

📬 Contact

Md Reazul Repon
Data Analyst | Power BI | SQL | Python
📧 Email: (add your email)
🔗 GitHub: https://github.com/MReza07

📄 License

This project is released under the MIT License.
