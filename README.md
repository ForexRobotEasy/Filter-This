# Filter This

This code is a sample implementation of a Forex trading robot that filters news based on currency and impact, selects relevant news for the current chart, refreshes the news source at user-specified intervals, validates order inputs, and executes market, limit, stop, and trailing stop orders.

## Developer's Site

For detailed reviews and trading results of this product, please visit [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/filter-this-review-chart-specific-forex-software-with-news-filter/). Please note that ForexRobotEasy is not the official developer of this product. We only provide a sample code that can work as described in this product. To find the official developer of this product, please use MQL5.

## Import Libraries

The code imports the following necessary libraries:

- `stdlib.mqh`: Provides standard functions for handling errors and working with strings.
- `trade\trade.mqh`: Provides functions for placing orders and managing trades.
- `datetime.mqh`: Provides functions for working with date and time.

## Constants

The code defines the following constants for order types:

- `MARKET_ORDER`: Represents a market order.
- `LIMIT_ORDER`: Represents a limit order.
- `STOP_ORDER`: Represents a stop order.
- `TRAILING_STOP`: Represents a trailing stop.

It also defines constants for order parameters:

- `priceLevel`: The price level for the order.
- `stopLoss`: The stop loss level for the order.
- `takeProfit`: The take profit level for the order.
- `trailingStop`: The trailing stop level for the order.

## Functions

The code includes the following functions:

- `filterNews(string currency, int impact)`: Filters news based on the specified currency and impact. It implements news filtering logic using Forex Factory's economic calendar data.
- `selectNews()`: Selects news relevant to the current chart. It automatically identifies keywords and filters news accordingly.
- `refreshNews(int interval)`: Refreshes the news source at user-specified intervals.
- `validateOrderInputs(double price, double stopLoss, double takeProfit, double trailingStop)`: Validates the order inputs. It checks if the inputs are within acceptable ranges and displays error messages for invalid inputs. It returns true if all inputs are valid, otherwise false.
- `executeMarketOrder(double price)`: Executes a market order at the specified price. It uses the Trade library to place the order and displays order execution details and error messages if any.
- `executeLimitOrder(double price)`: Executes a limit order at the specified price. It uses the Trade library to place the order and displays order execution details and error messages if any.
- `executeStopOrder(double price)`: Executes a stop order at the specified price. It uses the Trade library to place the order and displays order execution details and error messages if any.
- `executeTrailingStop(double trailingStop)`: Executes a trailing stop with the specified trailing stop level. It uses the Trade library to set the trailing stop value and displays trailing stop execution details and error messages if any.

## Main Function

The main function `OnStart()` performs the following actions:

- Filters news based on preferred currencies and impact.
- Selects news relevant to the current chart.
- Refreshes the news source at user-specified intervals.
- Validates order inputs.
- If the order inputs are valid, it executes the following orders:
  - Market order
  - Limit order
  - Stop order
  - Trailing stop

Please note that this code is a sample implementation and may require modifications to work in a specific trading environment. For the official developer of this product, please refer to MQL5.
