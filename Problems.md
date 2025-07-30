1. For each of the following subsets of $\mathbb{F}^3$, determine whether it is a subspace of $\mathbb{F}^3$.

	(a) $A = \{(x_1, x_2, x_3) \in \mathbb{F}^3 : x_1 + 2x_2 + 3x_3 = 0\}$  
	(b) $B = \{(x_1, x_2, x_3) \in \mathbb{F}^3 : x_1 + 2x_2 + 3x_3 = 4\}$  
	(c) $C= \{(x_1, x_2, x_3) \in \mathbb{F}^3 : x_1 x_2 x_3 = 0\}$  
	(d) $D= \{(x_1, x_2, x_3) \in \mathbb{F}^3 : x_1 = 5x_3\}$

Solution: 
(a) Let $x,y \in \mathbb{F}^3$ such that $x = (x_1, x_2, x_3)$ and $y = (y_1, y_2, y_3)$. By using the addition properties, we have
	$$x + y = (x_1 + y_1, x_2 + y_2,x _3 + y_3)$$
In particular,
$$
	x_1 + 2x_2 + 3x_3  = 0 \text{ and }y_1 +2y_2 + 3y_3  = 0
$$
By adding two equations together we get
$$
	(x_1 + y_1) + 2(y_2 + y_2) + 3(x_3 + y_3) = 0
$$
This means $x + y \in A$. Now for $\lambda \in \mathbb{F}$ we have 
$$
	\lambda + 2(\lambda x_2) + 3(\lambda x_3) = 0
$$
This also means $\lambda x \in A$. Hence, $A$ is a subspace of $\mathbb{F^3}$. 

(b) Let $x,y \in \mathbb{F}^3$ such that $x = (x_1, x_2, x_3)$ and $y = (y_1, y_2, y_3)$. By using the addition properties, we have
	$$x + y = (x_1 + y_1, x_2 + y_2,x _3 + y_3)$$
However
		$$ (x_1 + y_1) + 2(x_2 + y_2) + 3(x_3 + y_3) = 8 \neq 4$$
This implies that $x + y \notin B$, hence, $B$ is not a subspace of $\mathbb{F}^3$.

(c) Let $(0,0,1), (1,1,0) \in C$, we have
$$
	(0 + 1)(0 + 1 )(1 + 0) = 1 \neq 0
$$
Therefore, $(0,0,1) +(1,1,0) \notin C$, hence $C$ is not a subspace of $\mathbb{F}^3$ 

(d) $D$ is a subspace of $\mathbb{F}^3$ as we can prove similarly from (a)


 2. Verify all assertions about subspaces in Example 1.35.

3. Show that the set of differentiable real-valued functions $f$ on the interval $(-4, 4)$ such that $f''(-1) = 3f(2)$ is a subspace of $\mathbb{R}^{(-4, 4)}$.

---

4. Suppose $b \in \mathbb{R}$. Show that the set of continuous real-valued functions $f$ on the interval $[0, 1]$ such that 
$$
\int_0^1 f = b
$$
is a subspace of $\mathbb{R}^{[0, 1]}$ if and only if $b = 0$.

---

5. Is $\mathbb{R}^2$ a subspace of the complex vector space $\mathbb{C}^2$?

---

6.  
(a) Is $\{(a, b, c) \in \mathbb{R}^3 : a^3 = b^3\}$ a subspace of $\mathbb{R}^3$?  
(b) Is $\{(a, b, c) \in \mathbb{C}^3 : a^3 = b^3\}$ a subspace of $\mathbb{C}^3$?

---

7. Prove or give a counterexample: If $U$ is a nonempty subset of $\mathbb{R}^2$ such that $U$ is closed under addition and under taking additive inverses (meaning $-u \in U$ whenever $u \in U$), then $U$ is a subspace of $\mathbb{R}^2$.

---

8. Give an example of a nonempty subset $U$ of $\mathbb{R}^2$ such that $U$ is closed under scalar multiplication, but $U$ is not a subspace of $\mathbb{R}^2$.
