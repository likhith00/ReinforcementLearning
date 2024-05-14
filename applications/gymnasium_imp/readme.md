#### Implementation of MPD in grid world
In this task, you'll be creating an environment following the Markov Decision Process (MDP) framework. It's a simple grid world similar to the previous exercise, but with two distinct types of terminal states: two positive (G) and one negative (T).

![Representation of flow of Value iteration and Policy iteration](https://github.com/likhith00/ReinforcementLearning/blob/main/applications/gymnasium_imp/Gridimage.png)

The rewards are structured as follows:

- R = 1 if the state (s) is the goal (G).
- R = -1 if the state (s) is a trap (T).
- R = 0 otherwise.

#### Some Description 
The agent initiates its journey from the cell labeled S. At each time step, the agent can choose to move upwards, rightwards, downwards, or leftwards. Upon reaching the goal (G), the agent receives a reward of 1, and the episode terminates. If the agent stumbles into a trap (T), the episode ends with a reward of -1. Additionally, actions that would lead the agent beyond the board's boundaries are ignored.


### packages required

Install requirements file 
`pip install -r requirements.txt`
