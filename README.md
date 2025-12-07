## 📊 Customer Support Complaints Analysis – Power BI Dashboard

This project presents an end-to-end Customer Support Complaint Analysis using a real-world inspired dataset. The goal is to help organizations monitor customer issue trends, evaluate SLA performance, and understand customer experience across channels, regions, and device types. The entire solution includes data cleaning, transformation, modeling, DAX measures, and an interactive Power BI dashboard.

## 🚀 Project Overview

Customer support teams handle large volumes of complaints through multiple channels such as email, chat, social media and calls. To improve service quality, it is essential to track complaint trends, SLA compliance, customer satisfaction, and resolution efficiency.

This Power BI report provides clear visibility into:

Total complaints received

Status & SLA performance

Complaints by region, channel, device, priority

Monthly complaint trends

Resolution time analysis

Team performance insights

## 📌 Key Features of the Dashboard

✔️ Overall KPIs

Total Complaints: 200

Open Complaints: 7

Closed Complaints: 25

Resolved Complaints: 115

Escalated Complaints: 5

In-Progress Complaints: 48

Avg. Resolution Time: 24.98 Hours

SLA Compliance: 37%

✔️ Complaint Distribution

By Region

By Status

By Channel (Call, Email, Social Media, Chat, USSD)

By Priority (Low, Medium, High, Critical)

By Device Type

By Plan Type

✔️ Time-Based Analysis

Month-on-Month (MoM) complaint growth

Monthly resolved complaints

Trend visualization for 12 months

## 📁 Dataset Information

The dataset includes the following important columns:

Column Name-----Description
TicketID----Unique ID for each complaint

CustomerID-----	Unique customer identifier

CreatedDate-----Complaint creation date

ResolvedDate-----Issue resolution date

Status-----Complaint status (Open, Closed, In-Progress, etc.)

IssueType-----Main category of complaint

SubIssue-----Detailed sub-category

Channel-----Mode of complaint (Call, Chat, Email, etc.)

Priority-----Urgency level

ResolutionTimeHours-----Hours taken to resolve

SLA_DeadlineHours-----SLA commitment hours

SLA_Compliance-----Yes / No / No Response

SatisfactionScore-----Customer feedback rating

AssignedTeam-----Team handling the complaint

Region-----Customer’s region

PlanType-----Postpaid / Prepaid categories

DeviceType-----Android, iPhone, MiFi, Tablet, etc.

ComplaintDescription-----Text details of complaint

## 🛠️ Tools & Technologies Used

Power BI Desktop

Power Query for data cleaning and transformation

DAX for calculated measures

Excel / CSV Dataset

Data Modeling (Star Schema)

## 📷 Dashboard Preview

(Screenshot already included above in GitHub repository)

## 📊 DAX Measures Used (Sample)

Total Complaints = COUNT('Dataset'[TicketID])

Open Complaints = 
CALCULATE(COUNTROWS('Dataset'), 'Dataset'[Status] = "Open")

SLA Compliance % =
DIVIDE(
    CALCULATE(COUNTROWS('Dataset'), 'Dataset'[SLA_Compliance] = "Yes"),
    COUNTROWS('Dataset')
)

## 🔍 Insights Summary

The highest complaint load comes from Low priority issues.

Region-wise, most complaints originate from Khulna.

Social Media and Email are the top complaint channels.

SLA performance is low (37%), indicating delayed resolutions.

Device-related complaints are dominated by Android users.

Complaints fluctuate significantly month to month, with peaks in March and July.

## 📦 How to Use This Project

Download the .pbix Power BI file from this repository.

Download the dataset (xlsx/csv) file.

Open the report in Power BI Desktop.

Explore filters, slicers, and visual reports.

Modify visuals or use your own dataset for customization.


## 📬 Contact

Md. Rezaul Repon

Data Analyst (Power BI | SQL | Python)

🔗 LinkedIn:www.linkedin.com/in/repon07

🔗 GitHub: https://github.com/MReza07

📧 Email: reazulrepon@gmail.com

