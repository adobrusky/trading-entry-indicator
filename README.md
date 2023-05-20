# Entry Helper PineScript Indicator

This PineScript code implements an indicator called "Entry Helper" that assists in identifying potential long and short entry signals based on certain conditions. It plots shapes on the chart to indicate potential entry points.

## Usage

1. Apply the indicator to your chart by copying and pasting the code into the PineScript editor.
2. Adjust the input parameters according to your preferences.

## Input Parameters

- **showLongs**: Determines whether to show long signals. Default: true.
- **showShorts**: Determines whether to show short signals. Default: true.
- **volumeSMALength**: Length of the volume simple moving average (SMA) used for comparison. Default: 50.
- **proximityThreshold**: Threshold value to determine if the candle is close enough to a price level. Default: 0.15.
- **engulfingThreshold**: Threshold value to determine if a candle is considered engulfing based on the previous candle's range. Default: 0.5.
- **priceLevelsString**: A comma-delimited list of price levels to consider. Default: "0.0".

## Calculation and Conditions

1. The code checks if the volume is sufficient based on an SMA. The volume must be no lower than 5% less than the average.
2. It calculates the buy and sell volume for the current and previous candles.
3. It calculates the average buy and sell volume for the previous and previous previous candles.
4. It calculates the open/close range and high/low range for the current and previous candles.
5. It checks if the current candle is close enough to any of the specified price levels, indicating support or resistance.
6. It defines functions to determine if the current candle is bullish or bearish based on certain conditions.
7. It plots shapes on the chart to indicate potential long and short entry points based on the following conditions:
   - For long entries:
     - The candle is bullish.
     - The current buy volume is greater than the average buy volume of the previous two candles.
     - The current sell volume is less than the average sell volume of the previous two candles.
     - The volume is sufficient.
     - The candle is close to a support level.
   - For short entries:
     - The candle is bearish.
     - The current sell volume is greater than the average sell volume of the previous two candles.
     - The current buy volume is less than the average buy volume of the previous two candles.
     - The volume is sufficient.
     - The candle is close to a resistance level.

## Notes

- This indicator is intended to assist in identifying potential entry points but should not be used as the sole basis for trading decisions. Additional analysis and confirmation are necessary. This indicator should be paired with analysis of market sentiment and market structure.
- Adjust the input parameters and conditions according to your trading strategy and preferences.
- Test the indicator thoroughly on historical data and in a simulated or paper trading environment before using it with real funds.

**Disclaimer:** This indicator does not guarantee profitable trades and should be used at your own risk. Always perform your own analysis and exercise caution in the financial markets.