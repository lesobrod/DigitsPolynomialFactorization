# Factorization of Polynomials from integer digits

Let $n,b\in\mathbb{N}$ and $P_{n_b}$ is polynomial whose coefficients *are digits* of $n$ in base $b$.  
Let $Q_{1}(x) \cdot Q_{2}(x) \cdots Q_{m}(x)$ - polynomial factorization (over integers) of $P_{n_b}$.  
I'm interested in *coefficients of such factorization*, especially *union of all factor's coefficients* $\mathcal{U}(n,b)$ of a given polynomial.  

Let $n$ successively increase from $1$. 
From  responses I learned that: 
 - $\mathcal{U}(n,b) \subseteq \{0, \dots, b-1\}$   
 iff there are no carries when multiplying prime factors of $n$ (in base $b$)
 - Any  integer  sooner or later will appear in some $\mathcal{U}(n,b)$
