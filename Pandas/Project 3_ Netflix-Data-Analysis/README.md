# 🎬 Netflix Data Cleaning & Analysis Project

A complete, interview-ready data analytics project that cleans, engineers features for, and explores a Netflix Movies & TV Shows dataset — demonstrating the full workflow expected of a Data Analyst / ML Engineer candidate.

## 📌 Project Overview

**Goal:** Analyze Netflix's content catalog to uncover business insights (content mix, top countries, genre trends, ratings distribution, growth over time) while showcasing data cleaning, feature engineering, exploratory data analysis (EDA), and visualization skills.

**Difficulty:** Intermediate → Advanced
**Estimated time:** 8–12 hours (full build) / minutes to review

> **Dataset note:** This repo ships with a **synthetic dataset** (`data/netflix_titles.csv`) generated to match the schema and quirks of the public [Kaggle Netflix Titles dataset](https://www.kaggle.com/datasets/shivamb/netflix-shows) (same columns, plus intentionally injected missing values, duplicates, and inconsistent date/string formatting). This makes every cleaning step in the notebook meaningful and reproducible without requiring a Kaggle download. To run this on the real dataset, download `netflix_titles.csv` from Kaggle and drop it into `data/` with the same filename — the notebook will run unchanged.

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python | Programming |
| NumPy | Numerical operations |
| Pandas | Cleaning & analysis |
| Matplotlib | Core visualizations |
| Seaborn | Statistical visualizations |
| Jupyter Notebook | Development |

## 📁 Folder Structure

```
Netflix-Data-Analysis/
│
├── data/
│   ├── netflix_titles.csv        # Raw (synthetic) dataset
│   └── cleaned_netflix.csv       # Cleaned + feature-engineered output
│
├── notebooks/
│   └── Netflix_Data_Analysis.ipynb   # Full, executed analysis notebook
│
├── images/
│   ├── content_type.png
│   ├── country_distribution.png
│   ├── yearly_trend.png
│   ├── genre_distribution.png
│   ├── ratings.png
│   ├── duration.png
│   ├── duration_box_violin.png
│   └── country_year_heatmap.png
│
├── README.md
├── requirements.txt
└── insights.md


## 🔍 What the Notebook Covers

1. **Project setup** — imports, folder structure, data loading
2. **Data inspection** — shape, dtypes, `head()`/`info()`/`describe()`
3. **Missing value analysis** — quantify and handle nulls (fill vs. drop)
4. **Duplicate handling** — detect and remove duplicate rows
5. **Data type conversion** — parse `date_added`, extract year/month/day
6. **String cleaning** — trim/standardize text columns
7. **Feature engineering** — `Content_Type`, `Movie_Duration_Minutes`, `Season_Count`, `Primary_Genre`, `Primary_Country`
8. **EDA** — core business questions
9. **NumPy analysis** — vectorized stats on movie duration (mean, median, percentiles)
10. **Pandas analysis** — `groupby`, `pivot_table`, `value_counts` for top countries/genres/directors/ratings
11. **Matplotlib visualizations** — line, bar, horizontal bar, histogram, pie
12. **Seaborn visualizations** — countplot, boxplot, violin plot, heatmap
13. **Advanced analysis** — multi-column pivot tables
14. **Business insights** — written takeaways (see `insights.md`)
15. **Export** — cleaned dataset to CSV

## 📊 Key Insights (from this run)

See [`insights.md`](insights.md) for the full write-up (20 insights). Headline numbers:
- Movies make up **67.5%** of the catalog vs. **32.5%** for TV Shows.
- **France** leads content production (83 titles), closely followed by Australia and Italy.
- Content additions **peaked in 2001** (61 titles).
- Average movie duration is **~127 minutes** (90th percentile: ~177 min).
- **Crime TV Shows** is the most common primary genre.

## 🧠 Skills Demonstrated

- Python programming
- NumPy numerical computing (vectorized ops, percentiles, aggregates)
- Pandas data cleaning & feature engineering
- Matplotlib data visualization
- Seaborn statistical visualization
- Business analytics & insight generation
- End-to-end, portfolio-ready project structure
