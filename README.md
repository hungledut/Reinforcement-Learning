# My practice code for Reinforcement Learning 🤖

## Markov decision process 🌑

The markov decision process is an extension of Markov chain, including 4 key components: $( S,A ,R, P)$ 

| Symbol        | Meaning       | 
| ------------- |:-------------:|
| $S$           | State Space   |
| $A$           | Action        |
| $R$           | Reward        | 
| $P$           | Probability   | 

A **trajectory** is the trace generated when the agent moves from one state to another: $\tau = S_0, A_0, R_1, S_1, A_1, R_2, S_2, A_2, R_3, S_3$ <br>
An **episode** is a **trajectory** that goes from the initial state of the process to the final one: $\tau = S_0, A_0, R_1, S_1, A_1, ... R_T, S_T,$ where T is the terminal state
