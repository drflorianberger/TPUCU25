# The Master equation

One of the most successful tools to describe stochastic processes of molecules and cellular events is continuous time Markov processes. These processes are memory-less, and the most simple realization can be explained by a two-state system.

Let's consider a system that can be in two states: state $(1)$ and state $(2)$. The system stochastically jumps between these two states.

```{figure} 2states.png
---
height: 120px
name: 2states
---
```

The jump process is described by two transition rates $k_{12}$ and $k_{21}$, which can be determined from the inverse mean waiting times in the state as

$$
k_{12} = \mean{t_1}^{-1}.
$$

The probability that the process jumps from $(1)$ to $(2)$ in the time interval between $t$ and $t+dt$ is given by

$$
k_{12} dt.
$$

Let's assign time-dependent probabilities $P_1(t)$ and $P_2(t)$ for the system to be in the corresponding states, respectively:

```{figure} 2statesP.png
---
height: 100px
name: 2statesP
---
```

An important and very useful quantity is the probability current, which represents the mean number of transitions per time.

$$
J_{12} = k_{12}P_1.
$$

Now, we consider a small time step $dt$ and ask, what could happen in that time step to the probability. There are only three things that can happen: i) the system remains in state $(1)$, ii) the system goes from state $(1)$ to state $(2)$, and iii) the system goes from state $(2)$ to state $(1)$. Therefore, we can write 

$$
P_1(t+dt) = P_1(t) - J_{12} dt + J_{21} dt
$$

$$
P_1(t+dt) = P_1(t)(1 - k_{12}dt) + P_2(t) k_{21} dt
$$

$$
\frac{P_1(t+dt)-P_1(t)}{dt} = - k_{12}P_1(t) + k_{21} P_2(t)
$$

...and in the limit for $dt \to 0$, we obtain the master equation

$$
\frac{d P_1}{dt} = - k_{12}P_1 + k_{21} P_2
$$

Similarly, for

$$
\frac{d P_2}{dt} = - k_{21}P_2 + k_{12} P_1
$$



An example:

```{figure} ex.png
---
height: 200px
name: ex
---
```
