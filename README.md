# 🎯 Donor Management & Fundraising Analytics Dashboard (Power BI)

A complete end-to-end Power BI analytics solution designed for non-profit and fundraising organizations.  
This dashboard provides deep insights into donor behavior, donation performance, recurring income, pledge overdue trends, payment methods, failed transactions, and donor segmentation.  

Built with a clean UI, dynamic filters, drill-through reports, and fully optimized DAX measures.

---

## 📌 Project Overview

This project converts raw donor and donation data into a professional multi-page analytical dashboard.  
It helps fundraising teams track donor activity, improve retention, recover failed donations, and plan targeted campaigns.

The dataset is a **realistic dummy dataset** created specifically for demo and portfolio purposes.

---

## 📚 **Key Features**

### 🔹 **1. Donation Summary**
- Total Donation, Donation Count, Avg Donation
- Year-over-year donation trend
- Donations by campaign
- Top recurring donors
- Detailed donation records table
- Dynamic filtering using *Donation Period*

### 🔹 **2. Pledge Overdue Summary**
- Overdue pledge aging buckets (0–30, 31–60, 61–90, 120+ days)
- Total pledges vs overdue pledges
- Overdue trend over the years
- Top overdue donors
- Outstanding pledge record table
- Frequency & status breakdown

### 🔹 **3. Monthly Income Report**
- Monthly donation income trend (Jan–Dec)
- Total active donors
- Recurring vs one-time donation comparison
- Campaign-wise and method-wise income distribution
- Detailed monthly table

### 🔹 **4. Donor Segmentation**
- Donor categories:  
  *New Donor, Lapsed Donor, Monthly Recurring Donor, One-time Donor, Corporate/Church/Community Donor*
- Segment-wise donation amount contribution
- Year-wise segment trend visualization
- Active donor count, new donor count, high-value donor count

### 🔹 **5. Donor Summary (Drill-Through Page)**
- Donor-specific donation insights
- First Donation Date & Last Donation Date
- Total donated & Avg donation
- Recurring vs One-time breakdown
- Donation timeline trend
- Donor engagement/touchpoint table (Email, Call, Event, etc.)

### 🔹 **6. Payment Method Analysis**
- Donation distribution by payment method  
  *(Credit Card, Bank Transfer, Wallet/Mobile Pay, Cash, Others)*
- Donation distribution by Engagement Type  
  *(Most Used, Stable Large Gifts, Younger Donors, Declining Trend)*
- Monthly donation trend by method
- Highlighting major payment contributors

### 🔹 **7. Failed Transaction Summary**
- Failed/Pending donation records
- Failure reasons (Card Declined, Bank Error, Insufficient Funds, etc.)
- Total failed amount & donor-level breakdown
- Payment method comparison for failures
- Donation period slicer for quick filters

---

## 📊 **Data Model (High-Level)**

**Tables Used:**
- **Donor** – Donor details and demographics  
- **Donation** – All donation transactions  
- **Pledge** – Recurring pledges and expected payments  
- **Communication** – Donor engagement touchpoints  
- **ProgramAllocation** – Fund allocation by program  
- **FailedReasons** – Lookup for failure categories  

**Model Relationships:**
Donor[DonorID] → Donation[DonorID]
Donor[DonorID] → Pledge[DonorID]
Donor[DonorID] → Communication[DonorID]
Donation[DonationID] → ProgramAllocation[DonationID]



---

## 🧮 **Highlighted DAX Measures**

```DAX
-- First Donation Date
First Donation Date =
CALCULATE(MIN(Donation[DonationDate]))

-- Last Donation Date
Last Donation Date =
CALCULATE(MAX(Donation[DonationDate]))

-- Total Donation Amount
Total Donation Amount = SUM(Donation[Amount])

-- Donation Count
Donation Count = COUNTROWS(Donation)

-- Recurring %
Recurring % =
VAR TotalDn = COUNTROWS(Donation)
VAR RecDn = COUNTROWS(FILTER(Donation, Donation[IsRecurring] = TRUE()))
RETURN DIVIDE(RecDn, TotalDn, 0)

-- Days Since Last Donation
Days Since Last Donation =
DATEDIFF([Last Donation Date], TODAY(), DAY)

-- Overdue Days (Pledge)
Overdue Days =
DATEDIFF(Pledge[ExpectedPaymentDate], TODAY(), DAY)

-- Overdue Aging Bucket
Overdue Aging =
SWITCH(
    TRUE(),
    [Overdue Days] <= 30, "0–30 Days",
    [Overdue Days] <= 60, "31–60 Days",
    [Overdue Days] <= 90, "61–90 Days",
    "120+ Days"
)



🚀 How to Use

Download the Power BI report file .pbix.

Download the dataset donor_dummy_data.xlsx.

Open the .pbix in Power BI Desktop.

Refresh data connections (point to your local Excel file).

Explore the dashboard pages and interactive slicers.


🛠️ Tech Stack

Power BI Desktop

Power Query

DAX (Data Analysis Expressions)

MS Excel

Data Modeling

UX/UI Visualization Layer



🎯 Business Impact

This dashboard helps non-profits:

Improve donor retention with clear donor history

Track recurring income more accurately

Recover failed or overdue pledges quickly

Make data-driven fundraising decisions

Identify high-value donors for special engagement

Optimize payment and communication strategies


👨‍💻Shubham Trivedi
Power BI Developer | Analytics | Data Modeling
