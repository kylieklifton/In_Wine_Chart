# Data Diary

## Where I got the data

I downloaded the Wine Monthly Data CSV from the TTB (Alcohol and Tobacco Tax and Trade Bureau) website:
https://www.ttb.gov/regulated-commodities/beverage-alcohol/wine/wine-statistics

The file was last updated January 22, 2026.

## What is this data?

TTB is part of the U.S. Treasury Department. They regulate alcohol production in the U.S. Wineries have to report their numbers to TTB every month as part of their federal permits. This isn't survey data - it's required reporting.

The data includes:
- Production (how much wine was made)
- Taxable Withdrawals (wine leaving the winery to be sold)
- Tax Free Withdrawals (exports, etc.)
- Stocks on Hand (inventory)

## What metric did I use?

I focused on "Taxable Withdrawals" because that's the closest thing to sales in this data. It's the volume of wine leaving bonded premises to be sold domestically.

## What I did with it

1. Loaded the CSV into pandas
2. Filtered to just the "Taxable Withdrawals" category
3. Added up all wine types (low alcohol, sparkling, etc.) to get a monthly total
4. Calculated year-over-year change for each month (comparing Jan 2024 to Jan 2023, etc.)
5. Counted how many months showed a decline

## Limitations

- This is domestic production data only. Imported wine (like French Champagne) is NOT included.
- "Taxable withdrawals" is wine leaving wineries, not actual retail sales to consumers
- The data is reported by wineries themselves

## What I found

53 out of 58 months (91%) since January 2021 have had year-over-year declines in wine taxable withdrawals.
