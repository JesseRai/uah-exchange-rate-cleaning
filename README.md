# Ukrainian Exchange Rate Validation and Cleaning

This project validates and cleans the historical UAH/AZN exchange rate data published by the National Bank of Ukraine. It removes holidays, corrects for flatlined values due to reporting lags, and isolates a clean, usable time series for economic data analysis.
**Source**: [National Bank of Ukraine](https://bank.gov.ua/ua/markets/exchangerate-chart?cn%5B%5D=AZN&startDate=06.01.1996&endDate=28.06.2025)

### Steps

1. Exported full historical UAH/AZN data as CSV.
2. Transformed raw date formats using Excel.
3. Removed repeated values due to holidays using [`holiday_scraper.py`](https://github.com/JesseRai/public-holiday-scraper/blob/main/holiday_scraper.py).
4. Flagged periods of flatlined data caused by reporting delays.
5. Leveraged known pegging of both UAH and AZN to USD to identify which sections are valid.
6. Removed erroneous periods based on economic logic.
7. Compared cleaned vs. original time series in Tableau and explained rationale for edits.
