**Sales & Payment Performance Dashboard (Power BI)**

An interactive Power BI dashboard designed to monitor key business metrics related to sales performance and customer payment behavior across multiple regions.
The project demonstrates the complete analytical workflow - from data modeling and ETL (Power Query) to DAX calculations, visual design, and business insights presentation.

**- Project Overview**

This dashboard helps visualize and track:

Sales performance over time (USD & units)

Cumulative sales by customer, region, and business unit

Sales vs. target comparison (% achievement)

Year-over-year (YoY) sales growth analysis

Payment status breakdown with overdue and on-time customer insights

The goal is to provide business users and analysts with a clear, interactive view of sales and payment performance aligned with the fiscal year (FY25).

**- Data Model**

The solution follows a Star Schema structure for efficient querying and reporting.

Type	Table Name	Description
Fact	Sales	Transactional sales data (amount, quantity, date, customer, etc.)
Dimension	Country-Hub-Region	Regional and geographical hierarchy
Dimension	Targets_FY25	Sales targets per customer and region
Dimension	Payment_Status	Payment categories and due dates
Dimension	Calendar	Fiscal calendar used for time intelligence (DAX)

**- Tools & Technologies**

Power BI Desktop – dashboard creation and visualization

Power Query (M) – data extraction, transformation, and loading

DAX (Data Analysis Expressions) – KPI measures and fiscal-year comparisons

Excel / CSV datasets – data sources for simulation

GitHub – project documentation and versioning

**- Key DAX Measures**

Examples of key DAX measures used in this project:

Total Sales = SUM(Sales[Sales_Amount])

YoY Sales Growth % =
VAR PrevYear = CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Calendar'[Date]))
RETURN DIVIDE([Total Sales] - PrevYear, PrevYear)

Sales vs Target % =
DIVIDE([Total Sales], [Sales Target])

**- Dashboard Features**

✅ Dynamic filters by region, business unit, and customer
✅ Drill-through pages for detailed customer payment analysis
✅ Visual indicators for overdue invoices and target achievement
✅ Interactive cards for KPIs (total sales, growth %, overdue %)
✅ Clean and consistent layout for quick insights

**- Key Learnings**

This project strengthened my skills in:

Data modeling and relationship design (Star Schema)

Building DAX measures for financial and performance analytics

Creating interactive and insight-driven dashboards

Designing visuals for clarity and business impact

**- Preview**

<img width="1902" height="1024" alt="sales_overview" src="https://github.com/user-attachments/assets/5ddaff8e-ac62-429d-9946-70806d69f4e8" />
<img width="1889" height="1017" alt="payment_status" src="https://github.com/user-attachments/assets/5647f303-8ab2-4b95-a191-be8e3e9aa73f" />
<img width="1904" height="1003" alt="model" src="https://github.com/user-attachments/assets/ab870bcb-bef6-4b4d-9629-c0c474b75714" />


- View full project: https://github.com/Marciner-dev/Power_BI_Customer_sales_and_Payments
- View all my projects: https://github.com/Marciner-dev
