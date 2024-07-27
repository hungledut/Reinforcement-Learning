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
An **episode** is a **trajectory** that goes from the initial state of the process to the final one: $\tau = S_0, A_0, R_1, S_1, A_1, ... R_T, S_T,$ where T is the terminal state <br>
**Reward** is the immediate result that our actions produce: $R_t$ <br>
**Return** is the sum of rewards that the agent obtains from a certain point in time (t) until the task is completed, represented by $G$ <br>
**Discount factor** is represented by $\gamma \in \[ 0,1 \]$ <br>
The return associated with a moment in time t is the sum (discounted) of rewards that the agent obtains from that moment. We are going to calculate $G_0$, that is, the return to the beginning of the episode: <br>
$G_0 = R_1 + \gamma R_2 + \gamma^2 R_3 + ... + \gamma^{T-1} R_T$
