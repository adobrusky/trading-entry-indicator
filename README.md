# VPA Entry Indicator PineScript Indicator

This PineScript code implements an indicator called "VPA Entry Indicator" that assists in identifying potential long and short entry signals based on volume and price action (VPA). It plots shapes on the chart to indicate potential entry points.

## Usage

1. Apply the indicator to your chart by copying and pasting the code into the PineScript editor.
2. Adjust the input parameters according to your preferences.

## Input Parameters

- **Show Long Signals**: Determines whether to show long signals. Default: true.
- **Show Short Signals**: Determines whether to show short signals. Default: true.
- **Volume SMA Length**: Length of the volume simple moving average (SMA) used for comparison. Default: 50.
- **Acceptable Volume Tolerance**: Percentage threshold value to determine if the volume is sufficient. Volume must be no lower than the average volume - tolerance % of average. Default: 0.05.
- **Proximity Threshold**: Cent threshold value to determine if the candle is close enough to a price level. Default: 0.15.
- **Strength Threshold**: Percentage threshold value to determine if a candle is considered strong based on the previous candle's range. Default: 0.5.
- **Directional Threshold**: Cent threshold value to determine the acceptable tolerance between the candle's wicks and body for directional analysis. Default: 0.05.
- **Price Levels**: A comma-delimited list of price levels to consider. Default: "0.0".

## Calculation and Conditions

1. The code checks if the volume is sufficient based on an SMA. The volume must be no lower than 5% less than the average.
2. It calculates the buy and sell volume for the current and previous candles.
3. It calculates the average buy and sell volume for the previous two candles.
4. It calculates the open/close range and high/low range for the current and previous candles.
5. It checks if the current candle is close enough to any of the specified price levels (based on the proximity threshold), indicating support or resistance.
6. It defines functions to determine if the current candle is bullish or bearish based on certain conditions.
7. It considers the directional analysis by comparing the lengths of the wicks and body of the candle to identify potential bullish or bearish signals.
8. It plots shapes on the chart to indicate potential long and short entry points based on the following conditions:
   - For long entries:
     - The candle is bullish.
     - The current buy volume is greater than the average buy volume of the previous two candles.
     - The current sell volume is less than the average sell volume of the previous two candles.
     - The volume is sufficient.
     - The candle is close to a support level.
     - The candle's wicks indicate a bullish direction.
   - For short entries:
     - The candle is bearish.
     - The current sell volume is greater than the average sell volume of the previous two candles.
     - The current buy volume is less than the average buy volume of the previous two candles.
     - The volume is sufficient.
     - The candle is close to a resistance level.
     - The candle's wicks indicate a bearish direction.

## Notes

- This indicator is intended to assist in identifying potential entry points but should not be used as the sole basis for trading decisions. You must derive your own price levels to input into the indicator for it to work. Additional analysis and confirmation are also necessary. This indicator should be paired with market sentiment analysis, market structure analysis, and fundamental analysis.
- Adjust the input parameters and conditions according to your trading strategy and preferences.
- Test the indicator thoroughly on historical data and in a simulated or paper trading environment before using it with real funds.

**Disclaimer:** This indicator does not guarantee profitable trades and should be used at your own risk. A high probability of the entries that are signaled result in successful trades when accurate price levels are used and the indicator is paired with additional analysis; however, the indicator will still occasionally miss good entries and signal poor entries so do not interpret the indicator's signals as law. Always perform your own analysis and exercise caution in the financial markets.