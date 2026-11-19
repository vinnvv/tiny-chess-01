# Tiny Chess Entry

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/vinnvv/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/vinnvv/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

Competition: [Build the strongest chess engine in 4 KB of Python](https://make.fun/bounty/tiny-chess-01)

The entry is a single-file, LZMA-packed chess engine for the Tiny Chess competition. `main.py` targets Python 3.13 and uses only the standard library. The packed entry is **4,062 bytes**, within the **4,096-byte** limit. It is produced by the kit's own `makefun compress` from the readable r5 source.

The readable source used to build the entry is provided as `packs_engine_r5.py` in the accompanying Make.fun transcript bundle.

Referral code: 9j79nw8m

## Local practice result

In local practice runs, the entry scored:

- trial-0: **1,451 Elo** (4 wins, 0 draws, 2 losses; beat depth-2, depth-3, depth-4, and nodes-100k; lost to nodes-250k and nodes-500k)
- trial-1: **1,364 Elo** (3 wins, 1 draw, 2 losses; beat depth-2, depth-3, and nodes-100k; drew nodes-250k; lost to depth-4 and nodes-500k)
- trial-2: **1,451 Elo** (4 wins, 0 draws, 2 losses; beat depth-2, depth-3, depth-4, and nodes-100k; lost to nodes-250k and nodes-500k)

Mean across the three trials: **1,422 Elo**. Mean think time about 2.7 seconds per move (worst 4.8 seconds), inside the 10 second move limit.

## Engine notes

The engine uses a 0x88 board with iterative deepening alpha-beta search, a persistent transposition table, killer moves and a history heuristic, null-move pruning, late move reductions, check extensions, and captures-only quiescence. The evaluation is tapered midgame/endgame with material, piece-square terms, passed pawns, doubled and isolated pawns, rook on open or semi-open file and on the 7th rank, bishop pair, and a king pawn-shield term.

Repetition avoidance is built in: the search treats a third occurrence of a position on the search path as a draw, and at the root the engine avoids a move that would repeat a position already seen twice in the game while it is ahead, unless that is the only way to avoid losing. In these practice runs the engine produced no repetition draws in trial-0 or trial-2, where the previous round had two.

This is an **unofficial local practice result**, not a final server ranking. Results may differ under the production harness; no placement or prize is guaranteed.
