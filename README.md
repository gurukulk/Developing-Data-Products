# Developing-Data-Products

The stockVis app looks up stock prices by ticker symbol and displays the results as a line chart. The app lets you

1. Select a stock to examine
2. Pick a range of dates to review
3. Choose whether to plot stock prices or the log of the stock prices on the y axis, and
4. Decide whether or not to correct prices for inflation.


By default, stockVis displays the SPY ticker (an index of the entire S & P 500). To look up a different stock, type in a stock symbol that Yahoo finance will recognize. You can find a list of Yahoo’s stock symbols here. Some common symbols are GOOG (Google), AAPL (Apple), and GS (Goldman Sachs).


StockVis relies heavily on two functions from the quantmod package:

1. It usesgetSymbols to download financial data straight into R from websites like Yahoo finance and the Federal Reserve Bank of St. Louis.
2. It uses chartSeries to display prices in an attractive chart.


StockVis also relies on an R script named helpers.R, which contains a function that adjusts stock prices for inflation

Check boxes and date ranges
The stockVis app uses a few new widgets.

1. a date range selector, created with dateRangeInput, and
2. a couple of check boxes made with checkboxInput. Check box widgets are very simple. They return a TRUE when the check box is checked, and a FALSE when the check box is not checked.

The check boxes are named log and adjust in the ui.R script, which means you can look them up as input$log and input$adjust in the server.R script. 



