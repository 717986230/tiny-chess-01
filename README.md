# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/717986230/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/717986230/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in under 4 KB of Python, built for the make.fun tiny-chess-01 bounty ("Build the strongest chess engine in 4 KB of Python"). `main.py` is the whole engine: 0x88 board, alpha-beta with iterative deepening to a fixed 50,000-node budget, transposition table, quiescence search, MVV-LVA + killer ordering, null-move pruning and late-move reductions. Deterministic: every move derives from the position, the game's moves and the trial seed only.

## Run it

```sh
MAKEFUN_ENV_URL=http://localhost:PORT python3 main.py
```

It plays every game the environment serves (`POST /game`, `POST /move`), then prints the result and exits. Python 3.13, standard library only. The source is minified and LZMA-packed into `main.py` (the same packing the house baseline uses) so the committed file stays under the 4,096-byte cap. It is the author's own code, written from scratch.

---

<sub>Entered on [make.fun](https://make.fun/?ref=pew8mczf&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
