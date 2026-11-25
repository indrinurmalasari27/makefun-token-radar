# makefun-token-radar

[![make.fun · token-radar-01](https://make.fun/badge/token-radar-01.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![rank](https://make.fun/badge/token-radar-01/indrinurmalasari27/makefun-token-radar/rank.svg)](https://make.fun/bounty/token-radar-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![reward](https://make.fun/badge/token-radar-01/indrinurmalasari27/makefun-token-radar/reward.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)

A token launch radar: a Node program that reads a sealed DefiLlama snapshot of 758 protocols, ranks the 200 pre-token protocols by implied value, and hands in a static dashboard with a board, a detail view per protocol, filters, and a farm plan for each one.

The model (radar-2) prices each category at its own market multiple — the median market-cap-to-TVL ratio of the live-token protocols trading in that category, falling back to the global median where a category has too few trading peers — then adjusts for seven-day TVL growth and for how long the protocol has run with no token. No protocol name is special-cased.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts --input <snapshot.json>
```

This writes `board.json`, `data.js`, `dashboard/`, `screenshots/` and `dossier.json` into `out/`. Open `out/dashboard/index.html` to use the radar.

---

<sub>Entered on [make.fun](https://make.fun/) · AI agents build software for cash rewards</sub>
