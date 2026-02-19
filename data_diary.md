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

I focused on "Taxable Withdrawals" — but understanding what this meant took multiple reads of the TTB documentation.

**My understanding evolved:**
1. First I thought it was "sales" — but it's not retail sales to consumers
2. Then I thought it was "production" — but that's a separate category in the data
3. Finally I discovered: it's wine shipped from wineries to stores for sale, representing their main stock

"Taxable Withdrawals" = wine leaving bonded winery premises to be sold domestically. It's the closest proxy to domestic wine demand, but it measures what wineries ship out, not what consumers actually buy.

## What I did with it

1. Loaded the CSV into pandas
2. Filtered to just the "Taxable Withdrawals" category
3. Added up all wine types (low alcohol, sparkling, etc.) to get a monthly total
4. Calculated year-over-year change for each month (comparing Jan 2024 to Jan 2023, etc.)
5. Counted how many months showed a decline

## Chart Design Choices

- **Y-axis on right side:** Moved the vertical axis to the right so the reader's eye follows the declining line toward the axis labels
- **Wine color (#722F37):** Used a burgundy/wine color for the line to reinforce the subject matter
- **Starting at 2014:** Cut 2012-2013 data because those early years weren't needed to tell the story — the decline starts in 2020, so 2014 provides enough context for the rise-and-fall arc

## Limitations

- This is domestic production data only. Imported wine (like French Champagne) is NOT included.
- "Taxable withdrawals" is wine leaving wineries, not actual retail sales to consumers
- The data is reported by wineries themselves

## What I found

53 out of 58 months (91%) since January 2021 have had year-over-year declines in wine taxable withdrawals.
