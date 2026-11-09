# BTC Short Straddle Dashboard

Single-file, browser-only dashboard tailored for BTC option sellers (especially short straddles) using live Deribit public data.

## What it shows
- Live BTC spot
- Gamma regime (Positive / Negative) + approximate gamma flip and net GEX
- **Short Straddle Favorability score** (heuristic based on gamma regime, proximity to max pain, ATM alignment, IV level)
- Call wall / Put wall
- Max pain for selected expiry + spot distance to it
- For selected expiry:
  - ATM strike & ATM IV
  - 1σ Expected Move (range the market is pricing)
  - Approximate ATM straddle mark price (breakeven context)
  - Days to expiry
- 25Δ Risk Reversal approximation
- Put/Call OI ratio, total OI, 24h volume
- Simple GEX profile bars (top strikes)
- Full OI + IV table by strike (ATM highlighted)

## How to run
1. Download `index.html`
2. Open it in any modern browser (Chrome / Firefox / Edge)
3. It fetches Deribit public endpoints directly and computes everything locally

No install, no backend, no API keys. Auto-refreshes every ~45 seconds.

## Notes for short straddles
- Positive gamma + spot near max pain = better pin / mean-reversion environment.
- Expected Move shows the 1σ range. Short ATM straddle typically needs price to stay inside roughly 0.8× that move (or inside the straddle premium breakevens).
- Favorability score is a simple heuristic — not a trading signal. Always manage delta, size, and risk.
- GEX uses the common dealer convention (calls positive, puts negative). Calculations are approximations from mark IV and open interest.

Not financial advice. Data from Deribit public REST API.
