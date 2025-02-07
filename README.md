# 🤖 DumbBots: Chain Reaction 🎮
---

## 📥 Installation

To install the `dumbbots` 📦, follow these steps:

1. Install the package using `pip`:
   ```bash
   pip install dumbbots
   ```

---

## 🛠️ Usage

Here’s how you can get started:

### 📜 Import the Game
```python
from dumbbots.chain_reaction import ChainReaction
```

### 🔧 Initialize the Game
```python
# Create a 5x5 grid for the game
length, width = 5, 5
chain_reaction = ChainReaction(length, width)
```

### ➕ Add Dots to the Board
```python
# Add a dot for Player 1 at position (2, 3)
chain_reaction.add_dot(2, 3, player_no=1)

# Add a dot for Player 2 at position (4, 4)
chain_reaction.add_dot(4, 4, player_no=2)
```

### ✅ Check Game Status
```python
# Check if the game is over
winner = chain_reaction.check_game_over()

if winner == -1:
    print("The game is ongoing!")
elif winner == 0:
    print("No winner yet!")
else:
    print(f"Player {winner} wins!")
```

### 🔁 Example Game Loop
Here’s an example loop for two players:
```python
while True:
    for player in [1, 2]:
        y, x = map(int, input(f"Player {player}, enter y and x: ").split())
        chain_reaction.add_dot(y, x, player_no=player)

        winner = chain_reaction.check_game_over()
        if winner != -1:
            if winner == 0:
                print("It's a draw!")
            else:
                print(f"Player {winner} wins!")
            break

    if winner != -1:
        break
```

🎮 Happy Gaming!

