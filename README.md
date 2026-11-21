# Premier League Performance Analytics

How many points does it take to win the Premier League, finish in the top four, or avoid relegation? This project uses historical league tables to compare those outcomes across seasons.

The historical analysis covers **33 completed seasons, from 1992–93 to 2024–25**, with **666 club-season records**. The original dataset includes a partial 2025–26 snapshot, which the analysis excludes.

## Key findings

| Finding | Result |
| --- | --- |
| Closest title race by points | Manchester City and Manchester United both finished with **89 points** in 2011–12. Manchester City won on goal difference. |
| Highest champion points total | Manchester City earned **100 points** in 2017–18. |
| Highest runner-up points total | Liverpool finished second with **97 points** in 2018–19, one point behind Manchester City. |
| Most runner-up finishes in the analysis | Arsenal finished second **9 times**. |

## What the analysis measures

- **Title race:** first- and second-place points, the gap between them, and title and runner-up finishes by club.
- **Top-four race:** fourth-place points and the gap between fourth and fifth.
- **Relegation survival:** 17th-place points and the gap between 17th and 18th, starting in 1995–96 when the league moved to 20 clubs.

The notebook reports actual point totals and uses points per match multiplied by 38 where comparisons need to account for the league's early 42-match seasons. It includes charts and exports summary tables for Power BI.

## Notebooks and data

| Notebook | Purpose |
| --- | --- |
| [Data extraction](premier_League_data_extraction.ipynb) | Collects league tables from Wikipedia using Requests and Beautiful Soup. |
| [Data cleaning and analysis](premier_league_competitiveness_project_clean.ipynb) | Uses pandas, NumPy, and Matplotlib to clean the standings, calculate season metrics, create charts, and export summary CSVs. |

To reproduce the analysis, install the dependencies in a Python environment with Jupyter:

```bash
pip install jupyter requests beautifulsoup4 pandas numpy matplotlib
```

Run the extraction notebook first. Update its CSV export path and the analysis notebook's CSV input path so they point to the same local file. Then run the analysis notebook from top to bottom. To reproduce the figures above, use the same completed-season cutoff of 2024–25.

**Olaoluwa Bamgbose** · Marine Science and Technology graduate working with Python, SQL, Excel, and Power BI. [LinkedIn](https://www.linkedin.com/in/bamgbose-olaoluwa-4a20a2290/)
