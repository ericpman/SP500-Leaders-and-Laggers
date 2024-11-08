# SP500-Leaders-and-Laggers

## Project Description:
This project analyzes recent performance trends among S&P 500 stocks by comparing them to the RSP Equal Weight ETF. The code filters stocks based on specific criteria, ranks them by their relative performance to RSP, and exports the results to an Excel file.

## Workflow Overview:
The S&P 500 stock list is pulled from Wikipedia at https://en.wikipedia.org/wiki/List_of_S%26P_500_companies. Before running the code, it’s a good idea to verify the URL to ensure it's up-to-date, as changes to the S&P 500 index may affect stock composition.

The script uses the yfinance library to retrieve stock data for a specified period (default: last 30 days). Stocks are filtered to include only those with a closing price between $10 and $400 and a trading volume of over 1,000,000 shares on the latest trading day. Each stock's performance is calculated relative to the RSP ETF, providing a ranked list of the best and worst performers.

The script outputs an Excel file (performance_with_sector_YYYY-MM-DD.xlsx) containing the complete performance list, saved in the working directory. Additionally, a preview of the top 5 and bottom 5 performing stocks, including their sector information, is displayed within the Jupyter Notebook.

## Libraries
To run this code, you’ll need to have the following libraries installed: yfinance, pandas, datetime, and dateutil.

## Notes
Stock symbols with class shares use a dash instead of a period (e.g., BRK.B becomes BRK-B) for compatibility with Yahoo Finance.
