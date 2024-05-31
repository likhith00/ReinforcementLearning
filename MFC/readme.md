### Introduction

In this notebook, we will implement Model Free control in Reinforcement Learning.

#### Model Free control

###### What is Model Free control ??
In Dynamic Programming, we have seen that all the dynamics of the environment are explicitly defined. What if only few of them are defined ? In this case, agent learns to make decisions soley based on the observed outcomes of actions without modelling.

Model-Free Control is often contrasted with Model-Based Control, where the agent learns a model of the environment and uses that model to plan and make decisions.

Some Popular Model-Free Control algorithms include:
1. **Q-Learning:** 
    **Algorithm:** Q-learning is an off-policy algorithm, meaning it updates the Q-values using the maximum possible future reward, regardless of the action taken by the current policy.</br>
    **Update Rule:** 
    ```math
    Q(s, a) ← Q(s, a) + α[r + γmax(Q(s', a')) - Q(s, a)]

2. **SARSA:**  
    **Algorithm:** SARSA is an on-policy algorithm, which means it updates the Q-values (action-value function) based on the action actually taken by the current policy. </br>
    **Update Rule:** 
    ```math
    Q(s, a) ← Q(s, a) + α[r + γQ(s', a') - Q(s, a)]

3. Deep Q-Networks (DQN)
4. Policy Gradient Methods (PGM)

In summary, Model-Free Control is a powerful approach to Reinforcement Learning that allows agents to learn effective policies without requiring a detailed understanding of the underlying environment. However, it requires careful consideration of the trade-offs between exploration, data efficiency, and policy quality.