# Williams Pro EA ReadMe File

## Description

This is the ReadMe file for the Williams Pro EA code. This code is an expert advisor (EA) for MetaTrader 4 that uses the WilliamsR indicator and the EMA indicator to generate buy and sell signals in the Forex market. The EA opens market orders based on the signals and also has a feature to modify stop losses to break even if the trade moves favorably.

For detailed reviews and trading results of the Williams Pro EA, please visit the [Forex Robot Easy website](https://forexroboteasy.com/forex-robot-review/williams-pro-ea-review-reliable-forex-trading-software/). Please note that Forex Robot Easy is not the official developer of this product. We only provide this code as a sample that can work as described in the product.

## Code Details

The code is written in MQL4 and consists of two main functions: OnInit() and OnTick().

### OnInit Function

The OnInit() function is the initialization function for the EA. It checks if the required indicators (WilliamsR and EMA) are available and initializes the indicator handles. If any of the indicators fail to load, an error message is printed and the initialization fails.

### OnTick Function

The OnTick() function is the main function of the EA that is executed on each tick of the price. It first retrieves the current values of the WilliamsR and EMA indicators.

Next, it checks for a buy signal based on the WilliamsR value being below -80 and the previous candle's close price being above the EMA. If a buy signal is detected, a market buy order is opened with the specified lot size, stop loss, and take profit levels.

Similarly, it checks for a sell signal based on the WilliamsR value being above -20 and the previous candle's close price being below the EMA. If a sell signal is detected, a market sell order is opened with the specified parameters.

After opening the orders, the code checks for any existing orders with the same symbol and magic number. It then modifies the stop loss levels of these orders to break even if the trade has moved favorably.

## Input Parameters

The code has the following input parameters that can be customized:

- StopLoss: The stop loss level in pips.
- TakeProfit: The take profit level in pips.
- LotSize: The lot size for the orders.
- MagicNumber: The magic number to identify the orders.

## Disclaimer

Please note that Forex Robot Easy is not the official developer of the Williams Pro EA. We only provide this code as a sample that can work as described in the product. To find the official developer of this product, please use the MQL5 marketplace.

For detailed reviews and trading results of the Williams Pro EA, please visit the [Forex Robot Easy website](https://forexroboteasy.com/forex-robot-review/williams-pro-ea-review-reliable-forex-trading-software/).
