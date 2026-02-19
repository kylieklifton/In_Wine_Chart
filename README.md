# In One Chart: U.S. Wine Market Decline

## For Dhrumil

**Start here:** `wine_analysis.ipynb` — this is the main analysis notebook

**Data files:**
- `wine_monthly.csv` — source data from TTB (monthly wine statistics 2012-2025)
- `wine_yearly.csv` — source data from TTB (yearly totals)
- `chart_yearly.csv` — cleaned data used for Datawrapper chart
- `chart_monthly_change.csv` — alternate version showing month-over-month change

**You can ignore:** Nothing — all files are relevant

## Data Source
Alcohol and Tobacco Tax and Trade Bureau (TTB) Wine Statistics
https://www.ttb.gov/regulated-commodities/beverage-alcohol/wine/wine-statistics

## Finding
U.S. wine shipments from wineries have fallen every year since 2020, dropping 20% from 743 million gallons to 594 million gallons in 2024.

## Important: Understanding "Taxable Withdrawals"
After re-reading TTB documentation multiple times, I learned that "taxable withdrawals" is NOT sales or production — it's wine shipped from wineries to retailers for sale. This represents the main stock going to stores, not what consumers actually purchase. See `data_diary.md` for my full learning process.

## Chart Design Choices
- Y-axis on right side (eye follows declining line to labels)
- Wine color (#722F37) for the line
- Chart starts at 2014 (2012-2013 not needed for the story)

## Notes
See `data_diary.md` for details on data provenance and methodology.
