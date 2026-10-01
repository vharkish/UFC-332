# UFC Bet Calculator

A single-page calculator for UFC fight-week betting research:

- **3-Leg Parlay Builder** — set two anchors, add as many alternative third legs as you want. Enter each fighter's moneyline odds and stake; parlay odds, payout, profit, and ROI% calculate live.
- **Single Fighters** — moneyline payout / profit / ROI per fighter.
- **UFC 332 preset** — fighter names autocomplete and pull in that week's odds automatically.
- **Auto-save** — everything persists in the browser via localStorage. "New event" clears the board for the next card.

No build step, no dependencies — just open `index.html`, or publish with GitHub Pages.

## Publish with GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under "Build and deployment", set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`, then Save.
4. Your site will be live at `https://<username>.github.io/ufc-bet-calculator/` within a minute or two.

## Math

- Decimal odds from American: `1 + odds/100` (positive) or `1 + 100/|odds|` (negative)
- Parlay decimal = product of leg decimals
- American from decimal: `+(d-1)*100` rounded (d ≥ 2)
- Payout = stake × decimal · Profit = payout − stake · ROI = profit / stake
