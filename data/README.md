# Korean Government-Bond Yield Data

The main analysis requires daily Korean three-year government-bond yield data covering January 2016 through August 2026.

The notebook expects the following files:

- `Korea_3Y_2016_2020.xls`
- `Korea_3Y_2021_2025.xls`
- `Korea_3Y_2026.xls`

Each file should contain two columns:

1. Date
2. Korean three-year government-bond yield

The notebook converts valid dates and yield values, removes summary rows, combines the three periods, and removes duplicate dates.

Place the files in the notebook’s working directory before running the analysis. The raw files are not included in this repository because redistribution rights have not been verified.

Other market series—including USD/KRW, US Treasury yields, DXY, VIX, and USD/CNY—are downloaded directly within the notebook.
