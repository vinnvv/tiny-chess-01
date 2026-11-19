# Tiny Chess Entry

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/vinnvv/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/vinnvv/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

Competition: [Build the strongest chess engine in 4 KB of Python](https://make.fun/bounty/tiny-chess-01)

The entry is a single-file, LZMA-packed chess engine for the Tiny Chess competition. `main.py` targets Python 3.13 and uses only the standard library. The packed entry is **3,729 bytes**, within the **4,096-byte** limit. It is produced by the kit's own `makefun compress` from the readable v4 source.

The readable source used to build the entry is provided as `packs/engine.py` in the accompanying Make.fun transcript bundle.

## Local practice result

In a local practice run (practice/trial-0), the entry scored **1,451 Elo**: 4 wins and 2 losses. Across all three local practice instances it scored 1,451 / 1,279 / 1,099 (mean 1,276). Deterministic replay succeeded.

This is an **unofficial local practice result**, not a final server ranking. Results may differ under the production harness; no placement or prize is guaranteed.
