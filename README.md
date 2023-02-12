# Snake
In this project, a neural network is trained to play snake using Reinforcement Learning algorithms, in our case DQN.
The point is getting 30 points by playing snake based on the information that a person can get when playing snake:
- number of points (positive integer)
- obstruction to the left, right and front (boolean)
- approximate location of fruit and head

Rewards:
- movement = -1
- fruit = 3.5 * sqrt(score)
- wall collision = -20
- self collision = -50

Best Score = 42

An agent playing our snake should receive no more information than a human player in order to fairly evaluate its effectiveness. Our agent can determine if there is a danger from one side and which side is the fruit. In other words, the Agent does not know the specific coordinates of the snake's location, but if he moves along the left wall, he understands that the wall is on the left, which is a danger, the same works for food, the Agent understands that the food is to the left of the snake's head, not knowing specific coordinates of the head and food. In the figure, you can see a situation from the game in which our Agent would know the following information: danger on the left, danger on the right, fruit on the right, fruit on top, which also coincides with the information that an ordinary person receives when playing, respectively, the most logical action would be to go ahead, which allows you to get the highest reward in this situation, equal to -1.

![image](https://user-images.githubusercontent.com/122884911/218313956-63ef6e65-310f-41cc-aefa-a396b726e85d.png)

