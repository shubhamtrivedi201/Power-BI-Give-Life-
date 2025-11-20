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
