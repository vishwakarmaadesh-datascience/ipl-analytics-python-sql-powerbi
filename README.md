# IPL Analytics Dashboard (2008–2026)

## Project Overview

This project performs end-to-end IPL data analysis using **Python, SQLite, and Power BI**. The dataset covers IPL seasons from **2008 to 2026** and focuses on extracting team performance, venue insights, toss impact, and match trends.

---

# Problem Statement

IPL data is spread across multiple seasons and contains several inconsistencies. The objective was to:

* Clean and preprocess raw IPL data.
* Perform exploratory data analysis (EDA).
* Generate business insights using SQL.
* Build an interactive Power BI dashboard.
* Identify patterns related to teams, venues, toss decisions, and match outcomes.

---

# Tech Stack

### Python

* Pandas
* NumPy
* Matplotlib
* Seaborn

### Database

* SQLite

### Visualization

* Power BI

### Development Tools

* Google Colab
* DB Browser for SQLite
* Power BI Desktop
* GitHub

---

# Project Workflow

Raw Dataset (2008-2026)
↓
Data Cleaning & Feature Engineering (Python)
↓
EDA & Insights
↓
SQLite Database Creation
↓
SQL Analysis
↓
Interactive Power BI Dashboard

---

# Data Cleaning and Feature Engineering

Performed using Python in Google Colab:

* Removed missing values.
* Standardized team names.
* Fixed inconsistent records.
* Removed duplicate entries.
* Created derived metrics.
* Exported cleaned dataset for SQL and Power BI.

Notebook screenshots:

# SQL Analysis

Performed in SQLite using DB Browser.

### Sample Queries

### Most Successful Teams

```sql
SELECT winner,
COUNT(*) AS wins
FROM matches
GROUP BY winner
ORDER BY wins DESC;
```

### Team Performance While Chasing

```sql
SELECT winner,
COUNT(*) AS chase_wins
FROM matches
WHERE win_by_wickets > 0
GROUP BY winner
ORDER BY chase_wins DESC;
```

### Home Ground Advantage

```sql
SELECT venue,
COUNT(*) AS wins
FROM matches
GROUP BY venue
ORDER BY wins DESC;
```
=
SQL query screenshots:

![SQL Queries](<img width="1472" height="1078" alt="sqlqueryss" src="https://github.com/user-attachments/assets/6f299087-6bff-4970-ab8c-6debd8c9f685" />
)

---

# Key Insights Found

## Team Insights

* Mumbai Indians emerged as one of the most successful franchises.
* Chennai Super Kings consistently maintained high win rates.
* Some teams performed significantly better while chasing.

## Toss Analysis

* Teams winning the toss won approximately 50% of matches.
* Chasing teams had a slightly higher success rate.

## Venue Analysis

* Mumbai hosted the maximum number of matches.
* Certain venues exhibited strong home advantage.

## Match Trends

* Total runs scored increased over the years.
* Recent seasons witnessed more aggressive batting performances.

## Player Insights

* Most Player of Match awards were dominated by elite players.
* Match-winning performances strongly influenced team success.

---

# Power BI Dashboard

## Page 1 – Overview Dashboard

Contains:

* Total Matches
* Total Seasons
* Total Venues
* Toss Impact %
* Bat First Wins
* Chase Win %

Visuals:

* Team Wins
* Runs by Season
* Matches by Season
* Runs by City
* Venue Distribution

Screenshot:

![Overview Dashboard](<img width="1918" height="1078" alt="PowerBI Dashboard Sample" src="https://github.com/user-attachments/assets/eebe6b9d-83fe-4a8a-91a9-5f7af6d3401e" />
)


# Major Challenges Faced

### Data Integration

The dataset was distributed across multiple files and seasons, requiring extensive preprocessing.

### Database Import Issues

Encountered difficulties while importing CSV files into MySQL and later migrated to SQLite for efficient querying.

### Dashboard Design

Choosing meaningful KPIs and interactive visuals required multiple iterations.

---

# Repository Structure

```
ipl-analytics-python-sql-powerbi
│
├── notebooks
│   ├── IPL_Data_Cleaning.ipynb
│ 
├── database
│   └── ipl_analysis.db
│
├── powerbi
│   └── IPL_Analytics.pbix
│
├── images
│   ├── page1_dashboard.png
│   ├── sql_queries.png
│
└── README.md
```

---

# Future Improvements

* Player-level analysis using ball-by-ball data.
* Orange Cap and Purple Cap trends.
* Win probability analysis.
* Interactive drill-through pages in Power BI.
* Predictive analytics and machine learning models.

---

# Author

**vishwakarmadesh-datascience**

End-to-End Data Analytics Project using Python + SQLite + Power BI.
