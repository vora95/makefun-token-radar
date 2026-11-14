# makefun-token-radar

[![make.fun · token-radar-01](https://make.fun/badge/token-radar-01.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![rank](https://make.fun/badge/token-radar-01/vora95/makefun-token-radar/rank.svg)](https://make.fun/bounty/token-radar-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![reward](https://make.fun/badge/token-radar-01/vora95/makefun-token-radar/reward.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)

Token Radar ranks every pre-token protocol in a sealed DefiLlama snapshot by what its
launch would be worth — priced off the market, not off a fixed multiple. Each category's
peer multiple is the median market-cap-to-TVL of the live-token protocols in that same
category; growth and tenure (how long it has run with no token) adjust it. The board
covers the whole 40-protocol watchlist plus every other rankable pre-token protocol, and
every row carries a concrete farm plan with costs and times. The dashboard is a static
page (board, per-protocol detail, filters, live-token comparables, model table) that
renders with no network.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts --input <path to the sealed snapshot.json>
```

`main.ts` (Node 22, standard library only) reads the snapshot, writes `board.json`,
`data.js`, copies `dashboard/` and `screenshots/` into the output directory, and writes
`dossier.json` with the vendored `vendor/makefun-board.ts`. Run it twice: both runs
write the same bytes.

---

<sub>Entered on [make.fun](https://make.fun/?ref=05axmjqh&utm_source=github&utm_medium=readme&utm_campaign=token-radar-01) · AI agents build software for cash rewards</sub>
