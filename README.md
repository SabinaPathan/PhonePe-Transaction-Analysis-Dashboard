# PhonePe-Transaction-Analysis-Dashboard — Power BI

Problem Statement

PhonePe is one of India's largest digital payments platforms. This project builds a multi-page interactive Power BI dashboard to analyze transaction volume, value, and failure patterns across PhonePe's core services — Home overview, Insurance, Loans, Money Transfer, and Recharge & Bills — helping stakeholders quickly spot growth trends, failure hotspots, and top-performing services.

Dataset

PhonePe transaction, insurance, loan, money transfer, and recharge/bill data for the period 01-01-2024 to 30-12-2024, structured into separate tables (All_Transactions, All_Users, Insurance, Loans, Money_Transfer, Recharge_Bills) and loaded directly into Power BI from CSV/Excel source files.

Tools Used


Power BI Desktop (data modeling, visuals, KPI cards, aggregation-based measures)
Excel/CSV (source data)


Dashboard Pages & Key Insights

1. Home (Overview)


Total Amount: 3,333M | Successful Transactions: 288K | Failed Transactions: 12K (out of 300K total)
Services vs Amount: Loans dominate transaction value at 102M, followed by Insurance (22M), Money Transfer (15M), and Recharge & Bills (2M) — Loans alone account for roughly 70% of total transaction amount across all services.
Failed Payment Reason: Wrong PIN is the single largest failure cause (33.76%), followed by Bank Denied (27.61%) and Insufficient balance — together these three reasons account for over 90% of all failed payments.
Date vs Amount trend: Monthly transaction amount is volatile rather than steadily growing, swinging between ~10.5M and 13.7M, with a clear peak in July (13.7M) and a dip in August (10.6M).


2. Insurance


Total Amount: 512.92M, with a 95.75% payment success rate (47.88K successful vs. 2.12K failed).
Transaction volume is fairly evenly split across four insurance categories (~126M–129M each), showing no single insurance product dominates.
Failed Payment Reason is nearly evenly split three ways: Server error (33.76%), Insufficient amount (33.66%), and Wrong PIN (32.58%) — unlike the Home page, no single cause dominates insurance failures.


3. Loans


Total Amount: 2.53bn — by far the largest contributor to overall PhonePe transaction value.
Transaction by Loan Type is almost perfectly balanced across Gold Loan (25.85%), Mutual Fund (25.75%), Auto Loan (25.36%), and Credit Score (23.04%) — no single loan product is over- or under-weighted.
Each loan type individually processes 622M–644M in transactions, reinforcing that Loans is the highest-value, most evenly-distributed service line.


4. Money Transfer


Total Amount: 363.07M across 150K transactions, with a 96% success rate (143.96K successful vs. 6.04K failed).
Transfer Type Share is evenly distributed across To QR Code (25.77%), To Self Account (25.4%), To Mobile Number (24.79%), and To UPI ID (24.04%) — users don't strongly favor one transfer method over another.
Top user (PP1087376) alone completed 10.9K transfers, with the top 10 users ranging from 8.1K–10.9K transactions each — useful for identifying high-frequency/power users.


5. Recharge & Bills


Total Amount: 48.71M across 50K transactions, with only 1.92K failed transactions (~3.8% failure rate) — the lowest failure rate of any service on the dashboard.
Count of Users by Recharge Type is almost perfectly even across Cable TV, Electricity Bill, DTH, and Mobile Recharge (each ~12.4K–12.6K users), showing balanced adoption across bill categories.
Monthly transaction amount fluctuates between 140K–200K, with a peak around July (186K), mirroring the mid-year peak seen on the Home page.


Cross-Dashboard Takeaways


Loans is the highest-value service by far (2.53bn), dwarfing Insurance, Money Transfer, and Recharge & Bills combined — any business prioritization should center here.
Wrong PIN and Bank Denied are the most common failure reasons overall, suggesting UX improvements around PIN entry and clearer bank-decline messaging could meaningfully reduce failed transactions.
July is a recurring peak month across multiple services (Home and Recharge & Bills), which could reflect a seasonal spending pattern worth investigating further.
Recharge & Bills has the lowest failure rate (~3.8%) of all services, while Insurance and Home show notably higher failure rates — a good candidate for a deeper root-cause comparison.


How to Explore

Since GitHub cannot render .pbix files natively, the screenshots in /Screenshots capture each page. To interact with the live dashboard, download PhonePe-Transaction-Analysis-Dashboard.pbix and open it in Power BI Desktop (free).

Files


PhonePe-Transaction-Analysis-Dashboard.pbix — the full Power BI report
/Screenshots — PNG exports of all 5 dashboard pages
README.md — this file
