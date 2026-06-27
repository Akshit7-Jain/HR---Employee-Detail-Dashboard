# HR Analytics Dashboard | Tableau 📊

A dynamic, interactive HR dashboard designed to give HR managers and 
People Analytics teams a complete view of their workforce — from 
high-level headcount KPIs to individual employee records.

The HR Analytics Dashboard is a visually engaging Tableau report built 
across two views: an **HR Summary** and an **Employee Detail** page. 
Together, they enable users to analyze workforce composition, monitor 
hiring and attrition trends over time, explore salary patterns across 
gender and education, and drill into department- and city-level 
breakdowns. The dashboard is intended for HR professionals, business 
partners, and data-driven people managers who need to understand 
workforce health at a glance while retaining the ability to explore 
individual employee data on demand.

---

 ![Dashboard Preview](https://github.com/Akshit7-Jain/HR---Employee-Detail-Dashboard/blob/main/HR%20dashboard%20Overview.png)
 
![Dashboard Preview](https://github.com/Akshit7-Jain/HR---Employee-Detail-Dashboard/blob/main/Employee%20Dashboard%20Details.png)

---

## Tools & Technologies

- 📊 **Tableau Desktop** — Primary data visualization and dashboard platform
- 🧮 **Tableau Calculated Fields** — Custom logic for Age, Age Group, 
  Status (Active/Terminated), Location (HQ vs. Branch), Length of Hire, 
  % Total Hired, and dynamic highlight measures
- 📂 **Data Source** — `dataset.csv` embedded within the `.twbx` packaged workbook
- 📁 **File Format** — `.twbx` for development and distribution; `.png` for dashboard previews

---

## Data Source

- **Source:** HR employee dataset (CSV)
- **Fields include:** Employee ID, First & Last Name, Gender, Age / 
  Birthdate, Department, Job Title, Education Level, Performance Rating, 
  Hire Date, Termination Date, Salary, City, State

---

## Dashboard Views

### 1. HR | Summary
High-level workforce overview with the following visuals:

- **KPI Tiles** — Total Hired, Active Employees, and Terminated 
  Employees with snapshot counts
- **Hired & Terminated Over Time** — Trend lines showing hiring and 
  attrition patterns year by year
- **Employees by Department** — Bar chart of headcount distribution 
  across all departments
- **HQ vs. Branch Split** — Breakdown of employees between the New York 
  HQ and branch locations across other states
- **Gender Ratio** — Visual representation of gender distribution 
  across the workforce
- **Age Group Distribution** — Grouped bar chart segmenting employees 
  into age brackets (<25, 25–34, 35–44, 45–54, 55+)
- **Education Level Breakdown** — Distribution of employees by 
  educational background
- **Employee by Education & Performance** — Cross-tab heatmap showing 
  how performance ratings vary across education levels
- **Salary by Education & Gender** — Comparative salary analysis 
  highlighting pay differences across education and gender
- **Age vs. Department Salary Correlation** — Scatter/correlation 
  chart exploring the relationship between age and salary by department
- **Geographic Map** — Employees plotted by city and state

### 2. Employee | Detail
Row-level employee directory with filters for deep-dive exploration:

- Searchable and filterable table of all employees
- Fields: Full Name, Gender, Age, Education Level, Job Title, 
  Department, Salary, Hire Date, Status, Location
- Supports HR use cases like reviewing active headcount, identifying 
  long-tenured employees, and auditing terminated staff

---

## Features & Highlights

**Business Problem Addressed:**
- Which departments have the highest headcount — and how has that 
  changed over time?
- What is the gender and education breakdown of the workforce?
- How do salary levels vary across education and gender?
- Which cities and states have the largest employee concentration?
- Who are the active vs. terminated employees, and what is the attrition 
  trend year-over-year?

**Goal of the Dashboard:**
To provide HR stakeholders with a single, interactive Tableau interface 
that replaces static headcount reports — enabling real-time filtering by 
department, location, gender, education, and employment status.

**Key Calculated Fields:**
| Field | Logic |
|---|---|
| Status | Active if Termdate is null, else Terminated |
| Age | DATEDIFF from Birthdate to Today |
| Age Group | Bucketed: <25, 25–34, 35–44, 45–54, 55+ |
| Location | New York = HQ, all others = Branch |
| Length of Hire | Years from Hiredate (to today or termination) |
| % Total Hired | Employee count as % of total workforce |

---

## File Structure
HR_dashboard_Made.twbx

├── HR dashboard Made.twb       # Tableau workbook (XML)

├── Data/

│   └── dataset.csv             # Embedded HR data (Hyper extract)

└── Image/

├── Logo.png

├── dashboard-summary-active.png

├── dashboard-records-active.png

└── ...                     # Navigation & UI icons


