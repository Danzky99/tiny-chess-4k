# tiny-chess-01 engine

A 4 KB Python chess engine (MIT). Original code, sunfish-inspired design.

- 0x88 board, own legal move generation (castling, en passant,
  promotion, check/checkmate/stalemate)
- Negamax alpha-beta with quiescence (captures, promotions, check
  evasions), transposition table, killer-move ordering, MVV-LVA
  captures, material + piece-square evaluation
- Fixed node budget per move (90,000 nodes): no clock, no randomness,
  so every trial replays deterministically
- `main.py` is an lzma-compressed payload of the readable source
  (`engine_src.py`, kept outside this submission); the packed file is
  4,094 bytes, within the 4,096 cap

## Grade it locally

From the kit directory:

    node cli/makefun.mjs grade-local --kit . --bot <this directory> --driver process --instances 1
