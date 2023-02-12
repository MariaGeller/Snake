# Snake
This is a Q-Learning-based model playing snake based on the information that a person can get when playing snake:
- number of points (positive integer)
- obstruction to the left, right, and front (boolean)
- approximate location of fruit and head

Rewards:
- movement = -1
- fruit = 3.5 * sqrt(score)
- wall collision = -20
- self collision = -50

Best Score = 42
