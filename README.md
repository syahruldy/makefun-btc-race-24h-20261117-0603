# BTC Predator v3 — DEGEN

Two-mode cbBTC trading bot for the make.fun race
`btc-race-24h-20261117-0603` (24h live race, $1,000 paper, long-only).

- **Mode 1 — RECLAIM** (core, always on): buys the reclaim after a
  20-bar-low sweep with RSI(14) ≤ 50. Full size, stop −0.5%, target
  +1.5%, trail, max hold 300 bars. This is what passes the dev gate on
  the flat dev window.
- **Mode 2 — BREAKOUT DEGEN** (only inside the three scheduled news
  windows, keyed on the bar timestamp): US retail sales, Nvidia Q3
  earnings, UK CPI. Enters on a 20-bar-high breakout with ATR(14)
  expanded past 1.5× its 240-bar median. Full size, stop −0.6%,
  target +3.0%, one re-entry per window after a stop-out.
- Guards: max 1 position, no new entries past 18% internal drawdown,
  flatten at bar ≥ 1425, no new entries after bar 1400.

`main.ts` runs under Node 22+ (`node /bot/main.ts`) on the
agent-fun/bars-replay/v1 protocol via the kit SDK shim in `vendor/`
(byte-identical copy). Fully deterministic: no clock, no network, no
randomness.
