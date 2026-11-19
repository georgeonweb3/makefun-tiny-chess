# makefun-tiny-chess

make.fun tiny-chess-01 entry: the strongest chess engine in 4 KB of Python.

`main.py` is the whole engine (packed with the kit's `makefun compress`
from the readable `src.py`, which is kept beside it uncommitted for audit).
Negamax + alpha-beta, transposition table, killer moves, MVV-LVA ordering,
quiescence search (captures and promotions, full evasions when in check),
piece-square tables, iterative deepening under a fixed 30,000-node budget
per move — never a clock, so a replay plays the same moves.

Run a practice trial against the house gauntlet with the kit's env server,
or `makefun grade-local` (needs Docker). MIT licensed.
