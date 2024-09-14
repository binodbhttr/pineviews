# ADX and DI with Dynamic Threshold

## Overview

This Pine Script indicator, **"ADX & DI with Dynamic Threshold,"** helps traders detect trends, trend reversals, and trend strength using the **Average Directional Index (ADX)** and the **Directional Indexes (DI+ and DI-)**. It incorporates a **dynamic threshold** calculated using the average ADX over a user-defined period, along with a **fixed minimum threshold**, making trend detection more flexible and adaptable.

---

## Key Features

- **ADX and Directional Indexes (DI+ and DI-)**:  
  ADX measures the **strength** of a trend, while DI+ and DI- measure the **direction** of the trend. High DI+ signals upward price strength, and high DI- signals downward price strength.

- **Dynamic Threshold**:  
  A threshold based on the average ADX over a certain number of periods, ensuring the indicator adapts to market conditions. The threshold is compared to DI+ and DI- to generate trend signals.

- **Fixed Minimum Threshold**:  
  A user-defined minimum threshold ensures that signals are only generated in markets with a certain level of trend strength, preventing false signals in low-trending markets.

- **Visual Highlights**:  
  The background color highlights:
  - **Green for potential uptrend**.
  - **Red for potential downtrend**.
  - **Orange when directional movement is strong but trend strength is weak**, helping traders avoid false signals in sideways markets.

- **Customization**:  
  Several input parameters allow for complete customization of the indicator, ensuring it can adapt to different timeframes and assets.

---

## How to Use

### Inputs

1. **Length (len)**:  
   This is the smoothing period used to calculate the ADX and DI+/- values.  
   - Range: 5 to 50 (default: 14).

2. **Threshold Period (th_period)**:  
   Determines the number of periods over which the dynamic ADX threshold is calculated.  
   - Range: 5 to 200 (default: 50).

3. **Fixed Minimum Threshold (fixed_th)**:  
   The minimum ADX value that must be exceeded for the indicator to trigger signals.  
   - Range: 10 to 40 (default: 20).

4. **Smoothing Method**:  
   Choose between **SMA** (Simple Moving Average) or **EMA** (Exponential Moving Average) for smoothing the true range and directional movement calculations.

### Plots

1. **DI+ (Green)**:  
   Indicates the strength of upward price movements.

2. **DI- (Red)**:  
   Indicates the strength of downward price movements.

3. **ADX (Navy)**:  
   Indicates the overall strength of the trend, regardless of direction.

4. **Dynamic Threshold (Gray)**:  
   The dynamic threshold used for comparing ADX values.

5. **Fixed Threshold Line**:  
   A dotted black line showing the user-defined minimum threshold for ADX.

### Visual Cues

- **Green Background**:  
  Indicates a potential **uptrend** when DI+ > DI- and ADX is above the threshold.

- **Red Background**:  
  Indicates a potential **downtrend** when DI- > DI+ and ADX is above the threshold.

- **Orange Background**:  
  Indicates that **DI+** or **DI-** are strong, but ADX is weak. This suggests a lack of trend strength despite directional movement, which could lead to false signals or choppy market conditions.

---

## Customization Tips

- **Adjust the length (len)** based on the volatility of the asset.  
  A lower `len` (e.g., 10) may be suitable for faster timeframes (like 5-min charts), while a higher value (e.g., 20-30) may work better on longer timeframes.

- **Use the threshold period (th_period)** to fine-tune the dynamic ADX threshold.  
  A higher value for `th_period` smooths the dynamic threshold over a longer period, making it more resistant to sudden spikes in volatility.

- **Fixed Threshold (fixed_th)** should be set based on the strength of trends you want to capture.  
  A higher value (e.g., 30-40) is more conservative and will only trigger signals in very strong trends.

---

## Example Usage

This indicator can be used to:

- **Identify trends**:  
  When the ADX crosses the threshold and DI+ or DI- is dominant, indicating an uptrend or downtrend.

- **Spot trend reversals**:  
  When DI+ and DI- cross each other with a strong ADX reading.

- **Avoid false signals**:  
  By recognizing when DI+ or DI- are strong, but the ADX is below the threshold (highlighted in orange).

---

## Conclusion

The **ADX and DI with Dynamic Threshold** indicator is a versatile tool for trend-following strategies. It adapts to market conditions using dynamic and fixed thresholds and provides clear visual signals to help traders make informed decisions about market direction and trend strength.

By adjusting the various input parameters, this indicator can be tailored to any asset class or timeframe, making it suitable for all types of traders, from scalpers to swing traders.

Feel free to experiment with different settings and incorporate this indicator into your trading strategy for enhanced market analysis.
