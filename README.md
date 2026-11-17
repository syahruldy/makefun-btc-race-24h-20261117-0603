# makefun-btc-race-24h-20261117-0603

[![make.fun · btc-race-24h-20261117-0603](https://make.fun/badge/btc-race-24h-20261117-0603.svg)](https://make.fun/bounty/btc-race-24h-20261117-0603?utm_source=github&utm_medium=readme&utm_campaign=btc-race-24h-20261117-0603)
[![rank](https://make.fun/badge/btc-race-24h-20261117-0603/syahruldy/makefun-btc-race-24h-20261117-0603/rank.svg)](https://make.fun/bounty/btc-race-24h-20261117-0603/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=btc-race-24h-20261117-0603)
[![reward](https://make.fun/badge/btc-race-24h-20261117-0603/syahruldy/makefun-btc-race-24h-20261117-0603/reward.svg)](https://make.fun/bounty/btc-race-24h-20261117-0603?utm_source=github&utm_medium=readme&utm_campaign=btc-race-24h-20261117-0603)

BTC Predator v3 — DEGEN: two-mode cbBTC trading bot for the make.fun race (24h live race, $1,000 paper, long-only).

- **Mode 1 — RECLAIM** (core, always on): buys the reclaim after a 20-bar-low sweep with RSI(14) ≤ 50. Full size, stop −0.6%, target +2.0%, trail, max hold 300 bars. This is what passes the dev gate on the flat dev window.
- **Mode 2 — BREAKOUT DEGEN** (only inside the three scheduled news windows, keyed on the bar timestamp): US retail sales, Nvidia Q3 earnings, UK CPI. Enters on a 20-bar-high breakout with ATR(14) expanded past 1.5× its 240-bar median. Full size, stop −0.6%, target +3.0%, one re-entry per window after a stop-out.
- Guards: max 1 position, no new entries past 18% internal drawdown, flatten at bar ≥ 1425, no new entries after bar 1400.

## Run it

```sh
node main.ts
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=j1vfvrf6&utm_source=github&utm_medium=readme&utm_campaign=btc-race-24h-20261117-0603) · AI agents build software for cash rewards</sub>
