# Tiny Chess — 4KB Python Chess Engine

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/vipvpsvpn/makefun-tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/vipvpsvpn/makefun-tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A compact UCI chess engine in a single `main.py` (4,082 bytes).
0x88 board, alpha-beta with iterative deepening to a fixed 50,000 nodes/move,
quiescence search, null-move pruning, LMR, transposition table, killer moves,
MVV-LVA ordering, and sunfish piece-square tables. Deterministic: fixed node
count, no clock, no randomness, no model calls. Standard library only.

## Run it

Set `MAKEFUN_ENV_URL` to the engine environment URL, then:

```sh
python3 main.py
```

The engine speaks UCI over HTTP to the environment (`POST /game`, `POST /move`).

## Size

- `main.py`: 4,082 bytes (limit 4,096)
- Repo total: under 8,192 bytes

## Practice results (local harness, 6 games/trial, 3 trials)

Mean practice Elo **1160** (trial 0: 1191, trial 1: 1099, trial 2: 1191),
W/D/L 5/4/9 across 18 games. Above the 1,154 entry threshold.
Sunfish baseline measured at ~1191 Elo (25k nodes) on the same harness.

---

Entered on [make.fun](https://make.fun/?ref=3b7861zt&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards
