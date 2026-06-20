# Air Gap MTF — Pine Script Indicators

A collection of Pine Script v6 indicators for TradingView. The project is split into two focused indicators that can be used independently or together.

---

## Indicators

### 1. `ema_levels.pine` — Air Gap MTF EMA Levels

Plots EMAs from multiple timeframes as horizontal lines directly on your chart. The gaps between lines are called **air gaps** — zones where price can move with less resistance. Larger air gaps generally mean more reward potential on trades.

#### Features

- **Multi-timeframe EMAs** — plots 4 EMAs across 4 configurable timeframes (default: 30min, 1hr, 4hr, 1D)
- **EMA table** — optional on-chart table showing all EMA values, current price, and distance (diff) from price, with colour-coded rows (off by default)
- **Alert settings** — built-in alert support
- **Full customisation** — control colours, line styles, label text, offsets, alignment, and text size for every EMA individually

#### Settings

| Group | What it controls |
|---|---|
| EMA settings | Source, timeframe selection, and EMA lengths for each of the 4 timeframes |
| Price level | Line drawing mode (from day start / offset / full chart), visibility toggles per EMA |
| Label | Text, colour, alignment, offset, and price display per EMA label |
| Table Display | Position, layout (Standard/Ordered), text size, header/row colours, diff colour coding |
| Price axis visibility | Which chart timeframes the indicator renders on (seconds, minutes, hours, days, etc.) |

#### Default EMA Configuration

| Timeframe | EMA 1 | EMA 2 | EMA 3 | EMA 4 |
|---|---|---|---|---|
| 30min | 5 | 12 | 34 | 50 |
| 1hr | 5 | 12 | 34 | 50 |
| 4hr | 5 | 12 | 34 | 50 |
| 1D | 5 | 12 | 34 | 50 |

#### Usage

1. Open TradingView Pine Script editor
2. Paste the contents of `ema_levels.pine`
3. Click **Add to chart**
4. Adjust timeframes, EMA lengths, and colours in the indicator settings to suit your setup

---

### 2. `key_levels.pine` — Daily Key Levels

Plots the key daily price levels as horizontal lines anchored to the candle where each level was set. Includes overnight session tracking (previous after-hours + today's pre-market) for PMH/PML.

#### Features

- **6 key levels** — YHOD, YLOD, PMH, PML, TDH, TDL
- **Overnight session tracking** — PMH/PML accumulate across the previous after-hours session and today's pre-market, then freeze at the regular session open
- **Anchored lines** — each line starts at the exact candle where the level occurred, not at the session start
- **Full customisation** — colour, line style, thickness, label text, and price axis display per level

#### Key Levels

| Level | Full name | Description |
|---|---|---|
| YHOD | Yesterday's High of Day | The highest price reached during yesterday's regular session |
| YLOD | Yesterday's Low of Day | The lowest price reached during yesterday's regular session |
| PMH | Pre-Market High | The highest price of the overnight period — from yesterday's regular session close through today's pre-market; frozen at the regular session open |
| PML | Pre-Market Low | The lowest price of the overnight period — from yesterday's regular session close through today's pre-market; frozen at the regular session open |
| TDH | Today's High of Day | The highest price reached so far during today's regular session |
| TDL | Today's Low of Day | The lowest price reached so far during today's regular session |

#### Default Line Styles

| Level | Style |
|---|---|
| YHOD / YLOD | Dashed |
| PMH / PML | Dotted |
| TDH / TDL | Solid |

#### Settings

| Group | What it controls |
|---|---|
| Key Levels | Show/hide all levels; per-level colour, thickness, line style, and price axis display |
| Label | Text size, label offset from last bar |
| Price axis visibility | Which chart timeframes the indicator renders on (seconds, minutes, hours, days, etc.) |

#### Usage

1. Open TradingView Pine Script editor
2. Paste the contents of `key_levels.pine`
3. Click **Add to chart**
4. Adjust colours and styles in the indicator settings to suit your setup

> **Note:** PMH/PML require extended hours data to be enabled on your TradingView chart. The levels only plot on intraday timeframes.

---

## Legacy

`daily_levels.pine` is the original combined script containing both EMA levels and key levels in a single indicator. It is kept for reference but the split scripts above are the actively maintained versions.
