# Banking Loan Risk Management Dashboard

A Power BI dashboard that helps a bank keep track of the loans it has given out, and how risky those loans are. This README explains the project in plain language — no banking or data background needed.

---

## 1. What problem does this solve?

When a bank lends money to people (a "loan"), there's always a chance the borrower won't pay it back. This is called **credit risk**. Banks need to constantly watch things like:

- How much money is currently out on loan?
- How many customers currently have active loans?
- What percentage of loans are going bad (not being repaid)?
- Which types of customers, locations, or loan products are riskier than others?

Instead of digging through spreadsheets, this dashboard turns that raw data into charts and numbers that anyone — an analyst, a manager, or an executive — can glance at and understand in seconds.

## 2. What's a "dashboard"?

Think of a dashboard like the dashboard in a car: instead of looking at raw engine data, you get a speedometer, a fuel gauge, and a few warning lights that summarize what's happening. This Power BI file does the same thing for the bank's loan data — it summarizes thousands of loan records into a handful of easy-to-read visuals.

**Power BI** is a tool made by Microsoft for building these kinds of interactive dashboards. The file in this repo (`Banking_Loan_Risk_Management.pbix`) is opened using the free **Power BI Desktop** application.

## 3. What's inside the dashboard?

The dashboard has **two pages** (like two tabs in a browser):

### Page 1 — Overview
A general health check of the loan portfolio (the full set of loans the bank has given out). It includes:
- **KPI cards** — big single numbers at a glance, such as total loan portfolio value, number of active loans, number of customers, and the default rate.
- **A trend chart** — shows how the loan portfolio has changed over time (by month/year).
- **Breakdown charts** — show how loans split by branch, loan type, and loan status.
- **Filters (slicers)** — dropdown/list controls that let you narrow the view down to a specific customer segment, income band, state, or risk bucket.

### Page 2 — Risk Analysis
A closer look at *where the risk is coming from*:
- **A funnel chart** — shows loans moving through stages (e.g., from applied → approved → active → defaulted), so you can see where drop-off happens.
- **Risk category breakdown** — shows what portion of loans fall into low/medium/high risk categories.
- **Risk by branch and customer segment** — helps identify which branches or customer groups carry more risk than others.

## 4. Key terms explained

| Term | Plain-English meaning |
|---|---|
| **Loan Portfolio** | The full collection of all loans a bank has given out, added together. |
| **Outstanding Balance** | How much money is still owed back to the bank right now. |
| **Active Loans** | Loans that are currently ongoing (not yet fully paid off or closed). |
| **Default Rate** | The percentage of loans where the borrower stopped paying back as agreed. A higher number means more risk. |
| **Risk Bucket / Risk Category** | A label (e.g., Low, Medium, High) showing how likely a loan or customer is to default, usually based on things like income, credit history, or loan size. |
| **Customer Segment** | A group of similar customers (e.g., "Salaried," "Self-Employed," "Retired") used to spot patterns in behavior. |
| **Branch** | A physical or regional office of the bank that issued the loan. |
| **Loan Type** | The category of loan — for example, Home Loan, Personal Loan, Auto Loan, or Business Loan. |
| **KPI (Key Performance Indicator)** | A single important number used to judge how well something is performing — like a report card score. |
| **Slicer** | An on-screen filter/dropdown that lets the viewer focus on a specific slice of the data (e.g., only loans from one state). |

## 5. What data powers this dashboard?

The dashboard pulls from a small set of connected tables, similar to linked spreadsheets:

- **Loan_Fact** — the core table of loan records (loan status, branch, amounts, etc.)
- **CUST** — customer details (age group, occupation, income band, state, risk bucket, segment)
- **PROD** — loan product details (loan type, risk category)
- **DateTable** — a calendar table used to group and trend data by month/year
- **Measures** — pre-built calculations such as Total Loan Portfolio, Active Loans, Outstanding Balance, Default Rate, and Customer count

These tables are linked together (a common data modeling pattern called a **star schema**), which lets the dashboard slice loan data by customer, product, branch, or time without duplicating information.

## 6. How to open/use it

1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free, Windows only).
2. Open `Banking_Loan_Risk_Management.pbix`.
3. Use the page tabs at the bottom to switch between **Overview** and **Risk Analysis**.
4. Click on any chart, bar, or slicer to filter the rest of the page — everything is interactive and connected.

## 7. Who is this useful for?

- **Risk managers** — to monitor default trends and flag risky segments early.
- **Branch managers** — to compare their branch's loan performance to others.
- **Executives** — to get a quick, high-level read on the health of the loan book without needing to read raw data.

---

*This dashboard is for demonstration/analysis purposes and uses sample banking data.*
