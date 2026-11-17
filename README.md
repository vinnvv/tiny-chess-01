# Tiny Chess Entry

The entry is a single-file, LZMA-packed chess engine for the Tiny Chess competition. `main.py` targets Python 3.13 and uses only the standard library. The packed entry is **3,533 bytes**, within the **4,096-byte** limit.

The readable source used to build the entry is provided as `packs/engine.py` in the accompanying Make.fun transcript bundle.

## Local practice result

In a local practice run, the entry scored **1,099 Elo**: 1 win, 2 draws, and 3 losses. Deterministic replay succeeded.

This is an **unofficial local practice result**, not a final server ranking. Results may differ under the production harness; no placement or prize is guaranteed.
