Donor Management & Fundraising Analytics — Power BI Report

One-line: Interactive Power BI dashboard for donor analytics and fundraising performance — donation trends, recurring pledges, failed transactions, payment-method analysis, and donor segmentation.

Summary

This project is a professional Power BI solution that provides a complete analytics suite for non-profits and fundraising teams. It converts transactional donation data into actionable insights for donor relations, finance, call center, and marketing teams. The dashboard helps identify loyal (recurring) donors, track overdue pledges, analyze monthly income, monitor failed payments for outreach, and segment donors for campaigns.

What’s included

Donor / Donation / Pledge / Communication / ProgramAllocation sheets (Excel) — sample dummy data used for demo.

Power BI report (.pbix) with 6 pages:

Donation Summary — KPI cards, donation trend, donations by campaign, recurring vs one-time breakdown, donor-level table.

Pledge Overdue Summary — aging, overdue totals, overdue donors table.

Monthly Income Report — month-by-month income, channel/campaign breakdown, YoY comparisons.

Payment Method Analysis — share and trend of payment methods, avg donation by method.

Failed Transaction Summary — failed transactions list, failure reason analysis, failed-amount KPIs.

Donor Segmentation — RFM-like segments (New, Lapsed, High-Value, Recurring), segment contribution charts.

Sample screenshots (from the report) to showcase layout and visuals.

Useful example DAX measures used in the report (First Donation Date, Last Donation Date, Recurring %, Total Donation Amount, Failure Rate, Days Since Last Donation, Overdue Aging bucket).

Key features & business value

Donor 360 view — rapid profile view with first/last donation, total given, donation trend, and communication logs.

Predictable income visibility — recurring donation analysis to measure reliable monthly income.

Pledge monitoring — overdue detection and aging buckets for proactive follow-up.

Operational insights — failed transaction reasons and amounts for donor-care outreach to recover revenue.

Segmentation for campaigns — identify high-value and lapsed donors for targeted reactivation or stewardship.

Finance-ready reporting — monthly income with program allocation for board/leadership review.

Data model (high-level)

Donor (DonorID, DonorName, Contact Info, Category, JoinDate, PreferredPaymentMethod)

Donation (DonationID, DonorID, DonationDate, Amount, PaymentMethod, CampaignName, Channel, IsRecurring, Status, Notes)

Pledge (PledgeID, DonorID, PledgeAmount, Frequency, LastPaymentDate, ExpectedPaymentDate, Status)

Communication (CommID, DonorID, CommType, CommDate, Notes)

ProgramAllocation (AllocationID, DonationID, ProgramName, AllocatedAmount)

FailedReasons lookup for failure codes

Relationships:
Donor[DonorID] -> Donation[DonorID], Donor[DonorID] -> Pledge[DonorID], Donation[DonationID] -> ProgramAllocation[DonationID], Donor[DonorID] -> Communication[DonorID].
