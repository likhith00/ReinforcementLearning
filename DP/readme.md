
## Introduction
The notebook Research_DP.ipynb is an implementation of Dynamic programming to find optimum policy for the given MDP.

lets discuss some classes/functions used in the code.

1. GridWorldMDP(class): This class represents the gridworld environment. It initializes with a given grid shape (default is a 4x4 grid) and creates a dictionary P to store transition probabilities and rewards for each state-action pair.
    1. init function : Initializes the MDP with the specified grid shape. It generates transition probabilities and rewards for each state-action pair and stores them in the P dictionary.
    2. render : Renders the gridworld by printing it to the terminal.
2. print_value: Print a value function array in a nice format.
3. print_deterministic_policy: Print a policy array in a nice format.
4. init_value: Returns a initialized value function array for given MDP.
5. random_policy: Returns the random policy for a given MDP. policy[x][y] is the probability of action with y for state x.
6. policy_evaluation_one_step: It takes  MDP, value function, policy, discount factor and computes one step of policy evaluation and returns Value function of policy.
7. policy_evaluation: It takes MDP, policy, discount factor, theta and Computes full policy evaluation until convergence and returns Value function of policy.
8. policy_improvement: It takes MDP, value function, discount factor and Computes greedy policy w.r.t a given MDP and value function and returns the policy
9. policy_iteration: takes MDP, discount factor, theta as arguments and Computes the policy iteration (PI) algorithm and returns value function, policy.
10. value_iteration: Computes the value iteration (VI) algorithm. Takes MDP, discount factor, theta as arguments and returns value function, policy.


## Theory (extracted from chatgpt and groq(llama3) ;) and equations from notes  

Note: The theory and the diagram is subject to correction

### MDP 
Markov's decision process: RL problems are often formulated as MDPs, which consist of states, actions, transition probabilities, and rewards. The agent interacts with the environment by taking actions, transitioning between states, and receiving rewards.
1. S is the set of environment states 
2. A is the set of possible actions 
3. P are the state transition probabilities 
4. R is the reward function and 
5. γ is the discount factor

### Goal
The goal in RL is to find a policy that maximizes the expected cumulative reward over time.

### Why DP ?? 
Dynamic programming (DP) in reinforcement learning (RL) is a method used to find optimal policies in environments modelled as Markov decision processes (MDPs). It involves solving the Bellman equations iteratively to compute the optimal value function or policy.

### Techniques in Dynamic programming

Here are two main techniques used to find the optimal policy in dynamic programming:

##### 1. Policy Iteration:

1. Policy Evaluation: Start with an initial policy and iteratively evaluate its value function until convergence. This involves updating the value function estimates for each state according to the current policy until they stabilize.
2. Policy Improvement: Once the value function has converged, improve the policy by selecting actions that maximize the expected return (e.g., by selecting the action with the highest value according to the current value function).
3. Policy Iteration: Repeat the process of policy evaluation and policy improvement until the policy no longer changes, indicating convergence to the optimal policy.

##### 2. Value Iteration:

1. Value Iteration: Instead of separate steps for policy evaluation and improvement, value iteration combines them into a single step. It updates the value function estimates for each state by iteratively applying the Bellman optimality equation, which calculates the maximum expected return achievable from each state.
2. Policy Extraction: After the value function converges, the optimal policy can be extracted by selecting actions that maximize the expected return from each state according to the current value function.

##### Representation of Both techniques

![Representation of flow of Value iteration and Policy iteration](https://github.com/likhith00/ReinforcementLearning/blob/main/DP/DP%20flow.png)
