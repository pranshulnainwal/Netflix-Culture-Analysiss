# 🎬 Netflix Culture Analysis — Content & Cultural Shift Dashboard
Data Analysis Project 
> Tools: `Python` `Pandas` `Matplotlib` `Seaborn` `SQL` `Power BI`

---

## 📌 Project Overview

This project analyzes Netflix's content library to uncover **cultural trends, audience targeting patterns, and content strategy shifts** over time. The analysis frames findings as **business insights** around how Netflix has evolved its content culture, boldness, and genre diversity.

---

## 🎯 Business Questions Answered

| # | Business Question | Analysis Done |
|---|-------------------|---------------|
| 1 | How fast is Netflix growing its content library year-over-year? | Titles added per year |
| 2 | Is Netflix a Movie platform or a TV Show platform? | TV Shows vs Movies — bar + pie chart |
| 3 | What genres dominate Netflix's catalog? | Top 10 genres by title count |
| 4 | How does rating vary across Movies vs TV Shows? | Rating breakdown by content type |
| 5 | What audience does Netflix primarily target? | Top 5 ratings distribution |
| 6 | Is Netflix becoming more genre-diverse over time? | Unique genres per release year (2008+) |
| 7 | Is Netflix shifting toward bolder, mature content? | TV-MA/R content % and volume growth by year |

---

## 🗂️ Project Structure

```
Netflix-Culture-Analysis/
│
├── README.md
├── netflix_culture_analysis.ipynb   # Main analysis notebook
├── netflix_sql_queries.sql          # SQL version of analyses
├── netflix_graphs.zip
├── data/
│   └── netflix_titles.csv           # Source dataset (Kaggle)
├── dashboards/
│   └── Netflix_Dashboard.pbix       # Power BI dashboard
│   └── dashboard_preview.png        # Dashboard screenshot
└── 
```

---

## 🔍 Analysis Breakdown

### 1. Data Loading & Libraries
```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
from collections import Counter
```
Dataset: `netflix_titles.csv` — 8,800+ records, 12 columns

### 2. Data Cleaning & Feature Engineering
- Converted `date_added` → datetime, extracted `year_added`
- Parsed `duration` into `duration_num` (int) + `duration_type` (`min` / `Season`) using regex
- Filtered to titles added **2000 onwards**
- Exploded `listed_in` (comma-separated genres) for granular analysis

### 3. Visualizations Built

| Chart | What It Shows |
|-------|---------------|
| Countplot — Titles per Year | Netflix content growth 2000–2021 |
| Bar + Pie — Movies vs TV Shows | Content type split |
| Horizontal Bar — Top 10 Genres | Genre dominance |
| Countplot — Rating × Content Type | Audience targeting by format |
| Pie — Top 5 Ratings | Overall rating distribution |
| Bar — Unique Genres per Year (2008+) | Genre diversity trend |
| Histogram — TV-MA content by year | Mature content distribution |
| Dual Line Chart — Bold Content Growth | % mature + volume of TV-MA/R by year |

---

## 📊 Key Findings & Business Insights

### 🚀 Content Growth
Netflix peaked content additions in **2018–2019**, aligning with its aggressive global expansion phase. Post-2020 shows a slowdown — quality over quantity shift.

### 🎬 Movies vs TV Shows
Movies dominate (~70%) but TV Show additions have been **accelerating since 2017** — Netflix is strategically investing in serialized content for subscriber retention.

### 🎭 Top Genres
**International Movies, Dramas, and Comedies** lead. This reflects Netflix's global-first content strategy to serve diverse regional markets.

### 🔞 Cultural Boldness — Core Insight
The share of **TV-MA and R-rated content has grown consistently since 2013**. This is a deliberate strategy — Netflix differentiates from traditional broadcast TV by offering content that pushes creative boundaries.

**Business Implication:** Netflix targets adult subscribers (18–45) as its core revenue segment. Mature content is a competitive moat against legacy platforms.

### 👥 Audience Targeting
TV-MA and TV-14 together account for **~60%+ of all content**. Family/Kids content is sparse — an underserved market segment with growth potential.

### 📈 Genre Diversity
Unique genre count per year has remained relatively **stable post-2015**, suggesting Netflix has standardized its genre framework rather than experimenting with niche categories.

---

## 🛢️ SQL Queries

> All notebook analyses are replicated in `netflix_sql_queries.sql`
---

## 📊 Power BI Dashboard 

Planned visuals mapped to notebook charts:
- **KPI Cards:** Total Titles | Movies % | TV Shows % | Mature Content %
- **Bar Chart:** Titles added per year
- **Donut Chart:** Movies vs TV Shows split
- **Horizontal Bar:** Top 10 Genres
- **Stacked Bar:** Rating × Content Type
- **Line Chart:** Mature content (TV-MA/R) growth over time
- **Bar Chart:** Unique genres per year
- **Slicers:** Year | Content Type | Rating | Genre

---

## 🛠️ Tech Stack

| Tool | Usage |
|------|-------|
| Python 3.x | Core analysis |
| Pandas | Data manipulation & feature engineering |
| Matplotlib | Custom chart styling |
| Seaborn | Statistical visualizations |
| Collections.Counter | Genre frequency extraction |
| SQLite + SQL | Reproducible reporting layer |
| Power BI Desktop | Stakeholder dashboard |
| Jupyter Notebook | Analysis environment |

---

## 📁 Dataset

- **Source:** [Netflix Movies and TV Shows – Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows)
- **Records:** ~8,807 | **Period:** 2000–2021

---

---

## 💡 Skills Demonstrated

- ✅ Data cleaning — datetime parsing, regex extraction, null handling
- ✅ Feature engineering — `year_added`, `duration_num`, `duration_type`, `genre_list`
- ✅ EDA with business question framing (not just plots — insights)
- ✅ Cultural trend analysis — connecting data to content strategy
- ✅ SQL layer for reproducible, stakeholder-ready reporting
- ✅ Power BI dashboard design

---

## 👤 Author

**Pranshul Nainwal**  
[GitHub](https://github.com/pranshulnainwal) 

---
*Built to demonstrate end-to-end data analytics skills — data wrangling, EDA, insight storytelling, SQL, and Power BI.*
