
# Composite Bullish/Bearish Metric with Real-Time Expected High/Low Arrows

This Pine Script indicator for TradingView is designed to combine multiple technical indicators into a single composite metric, providing clear buy and sell signals. The script also calculates expected high and low price levels when these signals are triggered, displaying them as horizontal arrows on the chart.

## Features

- **Composite Metric**: Combines the Relative Strength Index (RSI), Moving Average Convergence Divergence (MACD), Bollinger Bands, Simple Moving Average (SMA), Exponential Moving Average (EMA), Stochastic Oscillator, and Volume Spread Analysis (VSA) into a single metric.
- **Buy and Sell Signals**: Provides clear buy and sell signals based on the composite metric. These signals are enhanced with VSA to indicate whether the signal is supported by volume analysis.
- **Expected High/Low Levels**: Calculates and plots expected high and low levels based on the Average True Range (ATR) and momentum adjustments. These levels are visualized on the chart as horizontal arrows.
- **Real-Time Plotting**: The indicator dynamically updates and plots buy/sell signals and expected high/low levels in real-time as market conditions change.

## How It Works

### Parameters

- **RSI Length**: The period for calculating the RSI.
- **MACD Short Length**: The short period for the MACD.
- **MACD Long Length**: The long period for the MACD.
- **MACD Signal Length**: The signal line period for the MACD.
- **Stochastic Length**: The period for calculating the Stochastic Oscillator.
- **Bollinger Bands Length**: The period for the Bollinger Bands.
- **SMA Length**: The period for calculating the Simple Moving Average.
- **EMA Length**: The period for calculating the Exponential Moving Average.
- **ATR Length**: The period for calculating the Average True Range.
- **Projection Factor**: A multiplier used to project expected high/low levels.
- **Sensitivity Tuner**: Adjusts the sensitivity of the expected high/low calculations.
- **Arrow Length**: The number of bars the horizontal arrows should span.

### Composite Metric Calculation

The composite metric is calculated as the average of scores derived from the following indicators:

1. **RSI Score**: Normalized RSI value.
2. **MACD Score**: Normalized difference between the MACD line and the signal line.
3. **Bollinger Bands Score**: Position of the current price relative to the Bollinger Bands.
4. **Moving Averages Score**: Combines price normalization, SMA, and EMA crossovers.
5. **Stochastic Score**: Normalized Stochastic %K value.
6. **VSA Score**: Volume Spread Analysis adds or subtracts a small value based on the relationship between price movement and volume.

### Entry Conditions

- **Buy Signal**: Triggered when the composite metric is greater than or equal to 0.9, indicating strong bullish conditions.
- **Sell Signal**: Triggered when the composite metric is less than or equal to 0.1, indicating strong bearish conditions.

### Expected High/Low Calculation

When a buy or sell signal is triggered, the script calculates expected high or low levels using the ATR and a momentum adjustment based on the MACD difference. The sensitivity of this calculation can be tuned with the `Sensitivity Tuner` parameter.

### Plotting

- **Buy and Sell Signals**: Displayed on the chart as green "BUY" labels for buy signals and red "SELL" labels for sell signals. If VSA confirms the signal, an asterisk (`*`) is added to the label.
- **Expected High/Low Arrows**: Horizontal arrows are plotted at the expected high or low levels when a buy or sell signal is triggered. These arrows are green for expected highs and red for expected lows.

## Usage

1. **Apply the Script**: Add this script as an indicator to your TradingView chart.
2. **Customize Parameters**: Adjust the indicator parameters to fit your trading style and the asset being analyzed.
3. **Monitor Signals**: Watch for buy and sell signals on the chart. The expected high and low levels will guide you on potential price movements after the signal is triggered.
4. **Use Sensitivity Tuner**: Fine-tune the sensitivity of the expected high/low levels using the `Sensitivity Tuner` parameter to adapt to different market conditions.

## Example

After adding the indicator to your chart, you will see green "BUY" labels and red "SELL" labels at the points where the composite metric indicates strong bullish or bearish conditions, respectively. Alongside these signals, green or red horizontal arrows will appear, showing the expected high or low price levels based on the current market dynamics.

## Notes

- This indicator is designed to provide real-time signals based on a combination of well-known technical indicators. However, like all technical analysis tools, it should be used in conjunction with other analysis methods and risk management strategies.
- The script allows customization of key parameters, enabling traders to adapt the indicator to different timeframes and asset classes.
