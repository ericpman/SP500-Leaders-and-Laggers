# SP500-Leaders-and-Laggers
## This project analyzes the recent performance of S&P 500 stocks compared to the RSP Equal Weight ETF. The code filters stocks based on specific criteria, then ranks them from the best-performing to the worst-performing relative to RSP, and finally exports the results to an Excel file. The performance is percentage based.

Project Description:
This project pulls the S&P 500 list from Wikipedia. The URL is found here: https://en.wikipedia.org/wiki/List_of_S%26P_500_companies. For good measure, it is best practice to check this URL to ensure it is up to date with any changes that may have been made within the S&P500 index before running the code.

The symbols are then fed into Yahoo Finance using our yfinance library, and stock data is retrieved for a specified time range (the last 30 days by default) and performs the following steps:

Filters stocks to include only those with:
A closing price between $10 and $400
A trading volume of over 1,000,000 shares on the latest trading day
Compares each filtered stock's performance relative to the RSP ETF.
Exports the performance results to an Excel file, listing each stock’s performance as a percentage.
The output provides the top 5 and bottom 5 performing stocks, along with their sector information for easy reference.
Note that for symbols with class shares, '.' is replaced with '-' for accurate pulling from Yahoo Finance.

Installation
To run this code, you’ll need the following libraries:

yfinance
pandas
datetime
dateutil

The script will output:
An Excel file (performance_with_sector_YYYY-MM-DD.xlsx) with the complete performance list, saved in the same directory.
A preview of the top 5 and bottom 5 performing stocks, displayed within the Jupyter Notebook.

