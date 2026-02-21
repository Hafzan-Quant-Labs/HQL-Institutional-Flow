# HQL Institutional Flow
### by [Hafzan Quant Labs](https://github.com/HafzanQuantLabs)

> A professional-grade Smart Money Concepts indicator for TradingView, engineered for traders who analyze price from an institutional perspective.

---

## Overview

**HQL Institutional Flow** provides a complete suite of market structure and order flow tools in a single indicator. It automatically detects where institutional participants are likely accumulating and distributing positions, giving retail traders a structured edge in reading price action.

Built on Smart Money Concepts (SMC) methodology and written in Pine Script v5 with performance optimizations including bounded memory management, safe array iteration, and clean modular architecture.

---

## Features

| Feature | Description |
|---|---|
| 🏗️ **Swing Structure** | Detects BOS and CHoCH at the macro swing level |
| ⚡ **Internal Structure** | Detects BOS and CHoCH at the micro/internal level |
| 📦 **Order Blocks** | Identifies and tracks swing & internal order blocks in real time |
| 🕳️ **Fair Value Gaps** | Detects bullish and bearish imbalances across any timeframe |
| 〰️ **Equal Highs & Lows** | Flags liquidity resting above and below price |
| 💪 **Strong/Weak High & Low** | Tracks the most significant swing extremes for directional bias |
| 🎯 **Premium & Discount Zones** | Draws dealing range zones relative to current structure |
| 📅 **MTF Levels** | Overlays previous Daily, Weekly, and Monthly highs/lows |
| 🎨 **Color Themes** | Colored and Monochrome display modes |
| 🔔 **Full Alert Coverage** | Alerts for every structural event |

---

## Installation

1. Open [TradingView](https://www.tradingview.com) and go to the **Pine Script Editor**
2. Click **New** to create a blank script
3. Copy the contents of [`HQL_Institutional_Flow.pine`](./HQL_Institutional_Flow.pine)
4. Paste into the editor and click **Save**
5. Click **Add to chart**

---

## Settings

### Smart Money Concepts
| Setting | Description |
|---|---|
| Mode | `Historical` shows all past signals. `Present` shows only the most recent |
| Style | `Colored` or `Monochrome` color theme |
| Color Candles | Colors candles based on current internal trend bias |

### Internal Structure
| Setting | Description |
|---|---|
| Show Internal Structure | Toggle internal BOS/CHoCH display |
| Bullish / Bearish Structure | Filter to show `All`, `BOS` only, or `CHoCH` only |
| Confluence Filter | Filters out low-significance internal breakouts |
| Label Size | `Tiny`, `Small`, or `Normal` |

### Swing Structure
| Setting | Description |
|---|---|
| Show Swing Structure | Toggle swing BOS/CHoCH display |
| Bullish / Bearish Structure | Filter to show `All`, `BOS` only, or `CHoCH` only |
| Show Swing Points | Display HH, HL, LH, LL labels |
| Swing Length | Lookback period for swing detection (default: 50) |
| Show Strong/Weak High/Low | Display trailing swing extremes |

### Order Blocks
| Setting | Description |
|---|---|
| Internal Order Blocks | Toggle + set max number to display (1–20) |
| Swing Order Blocks | Toggle + set max number to display (1–20) |
| Order Block Filter | `ATR` or `Cumulative Mean Range` volatility filter |
| Order Block Mitigation | Use `Close` or `High/Low` for mitigation detection |

### Equal Highs / Lows
| Setting | Description |
|---|---|
| Bars Confirmation | Number of bars to confirm EQH/EQL |
| Threshold | ATR sensitivity for equal level detection (0–0.5) |

### Fair Value Gaps
| Setting | Description |
|---|---|
| Auto Threshold | Automatically filters insignificant FVGs |
| Timeframe | Set a custom FVG detection timeframe |
| Extend FVG | Number of bars to extend FVG boxes |

### Highs & Lows MTF
Toggle and style Daily, Weekly, and Monthly previous high/low levels independently.

### Premium & Discount Zones
Toggle zones and customize colors for Premium, Equilibrium, and Discount areas.

---

## Alerts

The following alert conditions are available:

- Internal Bullish / Bearish BOS
- Internal Bullish / Bearish CHoCH
- Swing Bullish / Bearish BOS
- Swing Bullish / Bearish CHoCH
- Bullish / Bearish Internal OB Breakout
- Bullish / Bearish Swing OB Breakout
- Equal Highs / Equal Lows
- Bullish / Bearish Fair Value Gap

To set up alerts: right-click on the indicator → **Add Alert** → select the desired condition.

---

## Technical Notes

This script includes several improvements over standard SMC implementations:

- **Bounded arrays** — rolling arrays are capped at 5,000 bars to prevent memory bloat on long charts
- **Safe deletion loops** — order block and FVG arrays are iterated in reverse to prevent index-shift bugs during removal
- **Array bounds guards** — all slice operations are clamped to valid bounds to prevent runtime errors
- **Extracted functions** — swing label drawing is separated from structure detection for cleaner architecture

---

## License

© Hafzan Quant Labs. All Rights Reserved.

Unauthorized copying, modification, distribution, or commercial use of this code is strictly prohibited without explicit written permission from Hafzan Quant Labs.

---

## Disclaimer

This indicator is for **educational and informational purposes only**. It does not constitute financial advice. Trading involves significant risk of loss. Always do your own research before making any trading decisions.

---

<p align="center">
  <b>Hafzan Quant Labs</b><br>
  Quantitative tools for serious traders.
</p>
