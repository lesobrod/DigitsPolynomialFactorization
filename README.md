# Factorization of Polynomials from integer digits

Let $n,b\in\mathbb{N}$ and $P_{n_b}$ is polynomial whose coefficients *are digits* of $n$ in base $b$.  
So $n=n_{0}n_{1}\dots n_{k} = n_{0}+n_{1}\cdot b+n_{2}\cdot b^2+\dots+n_{k}\cdot b^k \Rightarrow$  
$\Rightarrow  n_{0}+n_{1}\cdot x+n_{2}\cdot x^2+\dots+n_{k}\cdot x^k$  
Let $Q_{1}(x) \cdot Q_{2}(x) \cdots Q_{m}(x)$ - polynomial factorization (over integers) of $P_{n_b}$.  
I'm interested in *coefficients of such factorization*, especially *union of all factor's coefficients* $\mathcal{U}(n,b)$ of a given polynomial.  

Let $n$ successively increase from $1$. 
From  responses I learned that: 
 - $\mathcal{U}(n,b) \subseteq \{0, \dots, b-1\}$   
 iff there are no carries when multiplying prime factors of $n$ (in base $b$)
 - Any  integer  sooner or later will appear in some $\mathcal{U}(n,b)$

More specifically, we will interest when a given integer $z$ *first appears* in some $\mathcal{U}(n,b)$.  

In general, we could consider $b<0$.  
And here is partial table of first appearances of succesfull $z$ for $-10 \leq b \leq 10$:   

| -10 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 0 | -1 | -8 | -7 | -6 | -5 | -4 | -3 | -2 | 10 | 11 | 13 | 12 | 14 | 15 | 16 | 17 | -9 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| -9 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 0 | -1 | -7 | -6 | -5 | -4 | -3 | -2 | 9 | 11 | 10 | 12 | 13 | 14 | 15 | -8 | -10 | -9 |  |
| -8 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 0 | -1 | -6 | -5 | -4 | -3 | -2 | 8 | 9 | 10 | 11 | 12 | 13 | -7 | -9 | -8 |  |  |  |  |
| -7 | 1 | 2 | 3 | 4 | 5 | 6 | 0 | -1 | -5 | -4 | -3 | -2 | 8 | 7 | 9 | 10 | 11 | -6 | -7 |  |  |  |  |  |  |  |  |
| -6 | 1 | 2 | 3 | 4 | 5 | 0 | -1 | -4 | -3 | -2 | 6 | 7 | 8 | 9 | -5 | -6 |  |  |  |  |  |  |  |  |  |  |  |
| -5 | 1 | 2 | 3 | 4 | 0 | -1 | -3 | -2 | 5 | 6 | 7 | -4 | -5 | -7 | {-6, 8} | {-8, 10} | 9 |  |  |  |  |  |  |  |  |  |  |
| -4 | 1 | 2 | 3 | 0 | -1 | -2 | 4 | 5 | -3 | -4 | -5 | 6 | {-6, 7} |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| -3 | 1 | 2 | 0 | -1 | 3 | -2 | -3 | 4 | -4 | 5 | -5 | {-6, 6} | 7 |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| -2 | 1 | 0 | -1 | 2 | -2 | 3 | -3 | {-4, 4} | {-5, 5} | {-6, 6} |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 2 | 1 | 0 | -1 | 2 | -2 | 3 | -3 | {-4, 4} | {-5, 5} | {-6, 6} |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 3 | 1 | 2 | 0 | -1 | 3 | -2 | -3 | 4 | -4 | 5 | -5 | 6 | -6 | 7 |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 4 | 1 | 2 | 3 | 0 | -1 | -2 | 4 | 5 | -3 | -4 | 6 | -5 | {-6, 7} | 8 |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 5 | 1 | 2 | 3 | 4 | 0 | -1 | -2 | -3 | 5 | 6 | 7 | -4 | -5 | 8 | -6 | -7 |  |  |  |  |  |  |  |  |  |  |  |
| 6 | 1 | 2 | 3 | 4 | 5 | 0 | -1 | -2 | -3 | -4 | 6 | 7 | 8 | 9 | -5 | -6 | -7 |  |  |  |  |  |  |  |  |  |  |
| 7 | 1 | 2 | 3 | 4 | 5 | 6 | 0 | -1 | -2 | -3 | -4 | -5 | 7 | 8 | 9 | 10 | 11 | -6 | -7 | -8 |  |  |  |  |  |  |  |
| 8 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 0 | -1 | -2 | -3 | -4 | -5 | -6 | 8 | 9 | 10 | 11 | 12 | 13 | -7 |  |  |  |  |  |  |
| 9 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 0 | -1 | -2 | -3 | -4 | -5 | -6 | -7 | 9 | 10 | 11 | 12 | 13 | 14 | 15 | -8 |  |  |  |
| 10 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 0 | -1 | -2 | -3 | -4 | -5 | -6 | -7 | -8 | 10 | 11 | 12 | 13 | 14 | 15 | 16 | 17 |  |

Obviously there are patterns in this data, but it is difficult to figure out them yet.   
[Mathematica notebook](PolyFactorsGit.nb)   
Although Python (and eg Julia) is thought to work faster, in this case  
*factorization over integers* is very optimized and fast with Wolfram Language.  
[Detailed data for base 10](Base10.md)
