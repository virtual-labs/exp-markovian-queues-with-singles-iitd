## Introduction 
#### M/M/1 queue is one of the queue that can be modeled as birth death process, which is a specific type of continuous time Markov chain. It consists of a set of states {0, 1, 2,... \} denoting the 'population' of a system. State transitions occur as soon as a customer arrives or departs from the system. Specifically, when the system is in a state $n \geq 0$, the time until the next arrival is exponential random variable with rate $\lambda$. At a random arrival, system moves from state $n$ to $n+1$. When the system is in state $n \geq 1$, the time until the next departure is an exponential random variable with rate $\mu$. At a departure, the system moves from a state $n$ to $n-1$. The states denote the number of customers in the system. The density function of interarrival times and service times are assumed to be exponentially distributed with density function given, respectively as
#### $$a(t)= \lambda e^{-\lambda t}, $$
#### $$b(t)= \mu e^{-\mu t}. $$

#### Let n denotes the number of customers in the system. The rate of arrivals \lambda, and rate of service \mu, is fixed, regardless of the number of customers in the system. The flow balance equations for this system are
#### $$(\lambda+\mu)p_n=\mu p_{n+1}+\lambda p_{n-1}, \quad \text{for}~ n\geq 1,$$
#### $$\lambda p_0= \mu p_1. $$
#### Thus we can write $p_n$ as
#### $$p_n=p_0\left(\frac{\lambda}{\mu}\right)^n, \quad for~ n\geq 1. $$
#### Additionally, $$\sum_{n=0}^{\infty}{p_n}= 1, $$
#### yields $$p_0=\frac{1}{\sum_{n=0}^{\infty}{\rho^n}},$$ where $\rho= \frac{\lambda}{\mu}$ is the traffic intensity for a single server. 
#### This gives $$p_0=1-\rho, \quad for~ \rho<1,$$
#### and $$p_n=(1-\rho)\rho^n, \quad for~ \rho<1.$$
#### which is the full steady-state solution for the M/M/1 system. The existence of a steady-state solution depends on the condition that $\rho<1$ or $\lambda<\mu$. This is intuitive, for if $\lambda>\mu$, the mean arrival rate is greater than the mean service rate, so the system size increases without bound over time. Note that the system is perfectly balanced when $\lambda=\mu$, but is unsatble, since it has no spare service capacity to handle random variation in arrivals and services.
### Performance Measures:
* #### Average number of customers in the system $(L)$ is given by $$L= \sum_{j=0}^{\infty}{jp_j}=\frac{\rho}{1-\rho}.$$
* #### Average number of customers waiting in the queue for service $(L_q)$ can be obtained as $$L_q=L-\frac{\lambda}{\mu}.$$
* #### Average time a customer spends in the system $(W)$ is obtained using Little's law, $L=\lambda W$, and is given as $$W=\frac{1}{\mu-\lambda}.$$
* #### Average time a customer spends in the queue $(W_q)$ is obtained using Little's law, $L_q=\lambda W_q$, and is given as $$W_q=\frac{\rho}{\mu-\lambda}.$$
* #### For the service time random variable $X$, average service time of a customer $(E[X])$ can be evaluated as $$E[X]=\frac{1}{\mu}.$$
