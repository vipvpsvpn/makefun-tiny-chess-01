# Tiny Chess — 4KB Python Chess Engine

A compact UCI chess engine in a single `main.py` (4,082 bytes).
0x88 board, alpha-beta with iterative deepening to a fixed 50,000 nodes/move,
quiescence search, null-move pruning, LMR, transposition table, killer moves,
MVV-LVA ordering, and sunfish piece-square tables. Deterministic: fixed node
count, no clock, no randomness, no model calls. Standard library only.

## Run

Set `MAKEFUN_ENV_URL` to the engine environment URL, then:

```
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
