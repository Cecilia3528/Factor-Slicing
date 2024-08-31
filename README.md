# Factor-Slicing
The reversal factors in the A-share market, such as the commonly used Ret20 factor, have shown significant long-term cumulative returns, but they often experience short-term drawdowns, making them a ”thorny rose” in the hearts of quantitative researchers. In fact, if we can segment the reversal factors more precisely in Momentum and Reversal, we can take the best and leave the rest. This is the idea behind factor slicing. After this, we can have deeper insights into the market about the micro-level drives for Reversal, **which turn out to be large-order Ask orders.**

## The idea behind
The actions of major market players tend to reflect the market’s overall sentiment and are likely to influence the market’s direction in the near future.

## Construction Method
- For the selected stock S, retrieve its data for the past 20 days.
- Calculate the i-16th percentiles amount per trade for each day (i range from 1 to 15) for the stock.
- Sum the daily price changes for the 10 days with the highest percentile transaction amount per
trade, denoted as M_High.
- Sum the daily price changes for the 10 days with the lowest percentile transaction amount per
trade, denoted as M_Low.
- Reversal factor after Factor Slicing M = M_High − M_Low.
M is the improved Reversal factor.
