<div class="Image" align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/7/7d/Super_tic-tac-toe_rules_example.png" alt="Logo" width="150" height="150">
</div>
<h1 align="center">Nine-Board-Tic-Tac-Toe</h1>

## About: 
This project involves writing an agent to play Nine-Board Tic-Tac-Toe, a complex variant of the traditional Tic-Tac-Toe game. In this version, the game is played on a 3x3 array of 3x3 Tic-Tac-Toe boards. Players take turns placing their marks on the boards, with each move determining the board for the next move. The objective is to win by getting three-in-a-row on any of the nine boards. This assignment aims to enhance your understanding of artificial intelligence and game strategy by developing a competitive agent.

## Built With: 
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) 
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white) 
![Sockets](https://img.shields.io/badge/Sockets-EF0092?logo=rsocket&logoColor=fff&style=for-the-badge)

## Getting Started:

To get started with the project, copy the provided src.zip archive to your workspace and unzip it. Navigate to the src directory and compile the code using the following commands:
```sh
  cd src
  make all
  ./servt -x -o
```
You should then see something like this:
<div class="Image" align="center">
  <img src="https://github.com/aryaman-sakthi/Nine-Board-Tic-Tac-Toe/blob/main/Board.png" alt="Logo" width="300" height="300">
</div><br>
You can now play Nine-Board Tic-Tac-Toe against yourself, by typing a number for 
each move. The cells in each board are numbered 1, 2, 3, 4, 5, 6, 7, 8, 9.

To play against the computer opponent, open two terminal windows and use the following commands:
```sh
  # Run the server with port 12345
  ./servt -p 12345 -x

  # Play against the agent by typing this in a different terminal:
  python3 agent.py -p 12345

  # To play against a sophisticated player type this in the second terminal:
  ./lookt -p 12345
```

## Working:
Our program combines Alpha-Beta pruning with logic, object-oriented programming, and data structure functionality to create an artificially intelligent agent which can defeat other agents with above-average to good intelligence. Several classes along with data structures like 2D arrays and lists have been used to store the current board and game state information.

### Implementation:
The algorithm begins by evaluating the state of the current board. For every turn of the agent, a copy of the original board is made, and the best move is found by calculating efficiency of each legally allowed play on that board. 

<div class="Image" align="center">
  <img src="https://images.squarespace-cdn.com/content/v1/5a0c6978bff2001ef7581170/1513544600041-LK94ONS0M8TSFUFCPPNB/full-minimax-move-tree.png" alt="Logo" width="300" height="300">
</div><br>

We use Minimax, as explained above, and a custom-designed scoring logic to determine the most optimal move by finding all future moves post committing a move to the current board and assigning it a score based on how well its subtrees perform. We do this for all possible moves and choose the move with the highest score, as the agent will have a higher chance of winning by proceeding down the subtree.

This is repeated till the opponent wins or a move by the agent on the current board forms a winning combination, leading to the agent winning.

## Conclusion:
The Nine-Board Tic-Tac-Toe project offers an excellent opportunity to delve into the complexities of AI in a strategic game setting. By implementing an agent that utilizes Alpha-Beta pruning, Minimax algorithm, and custom scoring logic, we have created a competitive player capable of making intelligent decisions and outperforming average opponents. The project not only reinforces key concepts in artificial intelligence and game theory but also enhances understanding of object-oriented programming and data structure manipulation.

The approach of evaluating board states, predicting future moves, and calculating scores based on potential outcomes provides a robust framework for developing AI strategies in more complex games. The combination of theoretical algorithms and practical coding practices makes this project a valuable learning experience in both AI and software engineering.

Overall, the Nine-Board Tic-Tac-Toe project successfully demonstrates how advanced algorithms and thoughtful design can create an effective AI agent, showcasing the power and potential of artificial intelligence in game development.
