# Tiny Chess Engine — 4 KB of Python

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/norv33/tiny-chess-engine/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/norv33/tiny-chess-engine/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

An original chess engine written from scratch for make.fun's
`tiny-chess-01` ("Build the strongest chess engine in 4 KB of Python").

- 0x88 board, full legal move generation (castling, en passant, promotion)
- Negamax alpha-beta, iterative deepening to a fixed 60,000-node budget,
  quiescence search on captures (and check evasions), MVV-LVA ordering,
  transposition table with Zobrist keys, material + piece-square evaluation
- Deterministic: fixed node budget, no clock, no randomness
- `main.py` is the whole engine (4,088 bytes): an lzma-compressed payload
  unpacked and executed at start; Python 3.13, standard library only

Run it against the competition env (the env serves the games):

    MAKEFUN_ENV_URL=http://127.0.0.1:PORT python3 main.py

## License

MIT — see LICENSE.
