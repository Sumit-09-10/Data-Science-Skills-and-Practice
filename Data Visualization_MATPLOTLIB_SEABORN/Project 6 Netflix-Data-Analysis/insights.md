# 📊 Netflix Data Analysis — Business Insights

*Derived from `Netflix_Data_Analysis.ipynb` running on the cleaned dataset (1,123 titles after removing duplicates and unparseable rows from an original 1,225-row raw file).*

## Content Mix
1. **Movies dominate the platform** — 67.5% of titles are movies vs. 32.5% TV shows, roughly a 2:1 ratio.
2. TV Shows in this dataset run a **median of 4 seasons**, with the 75th percentile at 7 seasons — most series are short-to-mid format rather than long-running.
3. Movie runtimes average **127 minutes** (median 128), ranging from 60 to 189 minutes, with the 90th percentile at 177 minutes — a small tail of notably long films.

## Geography
4. **France leads content production** with 83 titles, closely followed by Australia (82) and Italy (81) — production is fairly distributed rather than dominated by a single country.
5. The **top 10 countries** (France, Australia, Italy, South Korea, Brazil, UK, Egypt, India, Canada, Spain) account for a large share of all titles, indicating concentrated sourcing even though no single country dominates.
6. About **9.4% of titles** have no recorded country, which should be flagged for data-quality follow-up in a production pipeline rather than silently dropped.

## Growth Over Time
7. Content additions **peaked in 2001** (61 titles), with a second high point around 2006 (53) — growth in this dataset is non-linear rather than a steady ramp.
8. There's a **sharp drop-off after 2023** (only 9 titles in 2024), consistent with the dataset's collection cutoff rather than an actual slowdown.
9. Multiple years (2001, 2006, 2011, 2022) show local peaks, suggesting **cyclical content-acquisition patterns** worth investigating against licensing cycles in real data.

## Genres
10. **Crime TV Shows** is the most frequent primary genre (110 titles), followed by Action & Adventure (95) and Dramas (91).
11. Genre distribution is fairly even across the top 10 categories (74–110 titles each) — no single genre overwhelmingly dominates the catalog.
12. **Anime and Kids' TV** each account for a meaningful share (75 and 74 titles respectively), pointing to deliberate investment in family and niche-audience content.

## Ratings
13. **TV-14** is the most common rating (150 titles), followed closely by TV-G (136) and NR (135) — the catalog is reasonably balanced across audience maturity levels rather than skewing heavily toward one segment.
14. Mature-audience ratings (TV-MA, R) together account for roughly a fifth of titles, while family-friendly ratings (TV-G, TV-Y, PG) collectively make up a comparable share — the catalog serves a broad age range.

## Talent & Data Quality
15. About **30% of titles have no listed director**, the single largest data-quality gap in the dataset — a real-world equivalent would need a strategy (imputation, flag, or exclusion) before director-level analysis is trusted.
16. Among titles with a known director, the top contributors each appear **8–9 times**, suggesting a small group of prolific creators drive a disproportionate share of catalog volume.

## Data Cleaning Impact
17. **25 exact duplicate rows** were identified and removed during cleaning — a reminder that raw catalog exports commonly contain re-listed or re-ingested titles.
18. Roughly **100 rows** were dropped for missing `date_added` or `rating` values, since these fields could not be reliably imputed without introducing bias.
19. Standardizing country strings (trimming whitespace, fixing casing) was necessary before any groupby/aggregation — inconsistent text formatting alone can silently fragment "the same" category into several rows.

## Takeaway
20. The overall picture is a **movie-heavy, genre-diverse catalog** with content sourced from a broad set of countries, serving a wide range of audience maturity levels — but with real data-quality gaps (missing director/country) that any downstream analysis should account for.

---
*Note: This dataset is synthetic and randomly generated to mirror the Kaggle Netflix Titles schema for portfolio/practice purposes. Re-run the notebook against the real Kaggle CSV to get insights reflecting Netflix's actual catalog.*
