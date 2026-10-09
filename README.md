# Tic-Tac-Toe Agent

A Python learning project exploring a tabular, reward-based agent for command-line Tic-Tac-Toe.

## What is included

- A NumPy board representation and turn management.
- A state-action value dictionary.
- Random exploration and selection of higher-valued actions.
- Discounted rewards propagated through a game's move history.
- Training against a random opponent and terminal play against a human.
- Saving and loading learned values with pickle.

## Files

| File | Purpose |
| --- | --- |
| [TicTacToe.py](TicTacToe-ai/TicTacToe.py) | Board, moves and outcome checks |
| [Agent.py](TicTacToe-ai/Agent.py) | Training, rewards and action selection |
| [run.py](TicTacToe-ai/run.py) | Current training/play entry point |
| `brainX` | Previously saved value table |

## Run the existing entry point

```bash
git clone https://github.com/Kaan2a/TicTacToe.git
cd TicTacToe/TicTacToe-ai
python -m pip install numpy
python run.py
```

The entry point requests **100,000 training episodes** before terminal play. Human input uses board positions 1–9 in row order.

## Current limitations

This is an educational experiment. Win rates and playing strength have not been benchmarked.

The current entry point trains the O value table but configures the agent as X for human play, so the newly trained table and the loaded table differ. That configuration should be made consistent before evaluating the agent.

Training parameters, draw detection and edge cases also need targeted tests. The included pickle file should only be loaded if its origin is trusted.

