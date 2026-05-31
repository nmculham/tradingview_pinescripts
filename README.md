# Air Gap MTF — Daily Levels Indicator

A Pine Script v6 indicator for TradingView that plots EMA levels from multiple timeframes as horizontal lines directly on your chart. The gaps between lines are called **air gaps** — zones where price can move with less resistance. Larger air gaps generally mean more reward potential on trades.

## Features

- **Multi-timeframe EMAs** — plots 4 EMAs across 4 configurable timeframes (default: 30min, 1hr, 4hr, 1D)
- **Key levels** — plots Yesterday's High/Low (YHOD/YLOD), Previous Month High/Low (PMH/PML), and Today's High/Low (TDH/TDL)
- **EMA table** — on-chart table showing all EMA values, current price, and distance (diff) from price, with colour-coded rows
- **Alert settings** — built-in alert support
- **Full customisation** — control colours, line styles, label text, offsets, alignment, and text size for every level individually

## Settings

| Group | What it controls |
|---|---|
| EMA settings | Source, timeframe selection, and EMA lengths for each of the 4 timeframes |
| Price level | Line drawing mode (from day start / offset / full chart), visibility toggles per EMA |
| Label | Text, colour, alignment, offset, and price display per EMA label |
| Key Levels | YHOD, YLOD, PMH, PML, TDH, TDL — colours, line style, label, price axis display |
| Table Display | Position, layout (Standard/Ordered), text size, header/row colours, diff colour coding |
| Price axis visibility | Which chart timeframes the indicator renders on (seconds, minutes, hours, days, etc.) |

## Default EMA Configuration

| Timeframe | EMA 1 | EMA 2 | EMA 3 | EMA 4 |
|---|---|---|---|---|
| 30min | 5 | 12 | 34 | 50 |
| 1hr | 5 | 12 | 34 | 50 |
| 4hr | 5 | 12 | 34 | 50 |
| 1D | 5 | 12 | 34 | 50 |

## Usage

1. Open TradingView Pine Script editor
2. Paste the contents of `daily_levels.txt`
3. Click **Add to chart**
4. Adjust timeframes, EMA lengths, and colours in the indicator settings to suit your setup
