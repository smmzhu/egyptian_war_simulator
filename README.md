# Egyptian War Simulator

This code, written in Python, simulates the game of Egyptian War, and then analyzes the effect that a skill differential between two players would have on game length over the course of numerous iterations.

## Libraries used:
- seaborn
- pandas
- numpy

## How to run:
1. Setup an environment that is able to run `.ipynb` files and save `.csv`'s to the directory. Make sure you have all the libraries required at the top, or use an installer such as PIP to install them.
2. In the first cell, change the win rate to 0.5
3. In the second cell, change the win rate to 0.5
4. In the third cell, change the filename to `"50winRate.csv"`.
5. Run cells 1-3 (use shift+enter to run the code)
6. Repeat steps 1-4 but with 0.7 and `"70winRate.csv"` respectively.
7. Repeat steps 1-4 but with 1.0 and `"100winRate.csv"` respectively.
8. Run code boxes 4-6 for data analysis.

## Description of the code:

- Cell 1 writes the game logic (this version of Egyptian War only has the slap condition on doubles and sandwiches, and the automatic wins for losing to face cards). Cell 1 also runs the game 10000 times and save the game information to variable `data`.
- Cell 2 converts `data` to a dataFrame `df`, graphs the distribution of number of cards played per game, then prints the mean game length.
- Cell 3 saves the `df` to a local `.csv` file.
- Cell 4 reloads all the data from the `.csv` files back into a single new `df`.
- Cell 5 separates trials by each `win_rate` to juxtapose the game length distributions on a single graph.
- Cell 6 prints the mean game length per each `win_rate`.
