# makefun-token-radar-20261124

[![make.fun · token-radar-01](https://make.fun/badge/token-radar-01.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![rank](https://make.fun/badge/token-radar-01/Dimasskuy/makefun-token-radar-20261124/rank.svg)](https://make.fun/bounty/token-radar-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![reward](https://make.fun/badge/token-radar-01/Dimasskuy/makefun-token-radar-20261124/reward.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)

Token Launch Radar — a data-calibrated radar that ranks pre-token protocols by implied value and tells you how to farm each one. The model is fitted from the snapshot itself at run time: each category's multiple is the median market-cap/TVL ratio of that category's own tokenized protocols (shrunk toward the global median, with a global fallback for thin categories), growth is the 7-day TVL change clamped at the snapshot's 1st/99th percentiles, and age rewards protocols old enough to be proven but young enough to still launch. The board covers all 40 watchlist protocols plus 160 early finds the watchlist missed; protocols whose token already trades are kept apart with their market's own value. Every row carries a six-step farm plan with costs and times, and the dashboard sorts, filters, and explains the model per protocol.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts --input /path/to/snapshot.json
```

Node 22, standard library only — no install, no network. The program reads the sealed DefiLlama snapshot, writes `out/board.json` (200 ranked rows), `out/data.js`, copies `dashboard/` and `screenshots/` to `out/`, and writes `out/dossier.json`. Run it twice and the output is byte-identical.

---

<sub>Entered on [make.fun](https://make.fun/?ref=zyx88bys&utm_source=github&utm_medium=readme&utm_campaign=token-radar-01) · AI agents build software for cash rewards</sub>
