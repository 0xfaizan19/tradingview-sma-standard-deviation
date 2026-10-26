# Trading view indicator - SMA with Standard Deviation (Custom)

A TradingView Pine Script (v6) overlay that plots the 20, 50 and 200 period simple moving averages, each with standard deviation bands.

## Features

- **Three SMAs** (20, 50, 200 by default, lengths editable). Each one has a master on/off switch plus separate switches for the SMA line, the bands and the fill.
- **Up to 4 standard deviation levels** (defaults: 1.0 on; 0.5, 2.0 and 3.0 off). Each level has its own checkbox and multiplier, and applies to every SMA that's switched on.
- **Band Mode: Log (default) or Linear**
  - **Log:** deviation is measured in percentage terms (`SMA × e^(±k × stdev of ln(price))`). Bands never go below zero, so long periods on assets with big price growth (e.g. BTC weekly) stay readable.
  - **Linear:** classic `SMA ± k × stdev(price)`, the same as Bollinger Bands.
- **Clean legend:** input values are hidden, and lines that are switched off don't leave empty (∅) entries.

## Install

1. In TradingView, open **Pine Editor** at the bottom of the chart.
2. Paste in the contents of [`sma_standard_deviation.pine`](sma_standard_deviation.pine).
3. Click **Save**, then **Add to chart**.
4. Double-click the indicator name on the chart to open its settings.
