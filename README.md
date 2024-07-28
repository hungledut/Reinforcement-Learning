# Reinforcement Learning beginner to master - AI in Python (Udemy) 🤖

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
$G_0 = R_1 + \gamma R_2 + \gamma^2 R_3 + ... + \gamma^{T-1} R_T$ <br>
**Policy** is a function that takes a state as input and returns the action to be taken in that state: $\pi : S \mapsto A$ <br>
The **Policy** has 2 ways to express: (1) Probabilities of taking action $a$ in state $s$: $\pi(a|s)$ (2) Action $a$ taken in state $s$: $\pi(s)$ <br>
There are two types of **policy** : (1) Stochastic Policy (2) Determnistic Policy <br>
(1) Stochastic Policy $\pi(s) = [p(a_1),p(a_2),...,p(a_n)]$. For example: $\pi(s) = [0.3, 0.2, 0.5]$ <br>
(2) Deterministic Policy $\pi(s) \mapsto a$. For example: $\pi(s) = a_1$ <br>
To maximize the sum of *discounted* rewards, we have to find the optimal **policy** $\pi_*$ <br>
The **value of a state $v_{\pi}(s)$** is defined as the **return** that we expect to obtain from that state $s$ and interacting with the environment following policy $\pi$ until the end of episode: 
$v_{\pi}(s) = \mathbb{E}[G_t|S_t=s] = \mathbb{E}[R_{t+1} + \gamma R_{t+2} + \gamma^2 R_{t+3} + ... + \gamma^{T-t-1} R_T|S_t=s]$
