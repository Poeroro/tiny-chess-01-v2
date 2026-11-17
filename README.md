# tiny-chess-01 — v2 engine

A chess engine in 4,068 bytes of Python for make.fun's tiny-chess-01,
written from scratch for this competition.

`main.py` is the whole engine: a 0x88-mailbox negamax alpha-beta search
with a transposition table, quiescence over captures, MVV-LVA and killer
move ordering, and piece-square-table evaluation. It searches to a fixed
budget of 40,000 nodes a move — never a clock — so every trial replays
move for move. The readable source is packed into `main.py` as an
lzma + base85 payload with its unpacker; Python 3.13, standard library
only, and it reads no other file.

Local practice trials against the house ladder: Elo 1464 and 1396.
