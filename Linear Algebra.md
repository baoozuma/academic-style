# 1 - Vector Space

> [!Definition] Definition 1
>  (Vector space)*: A triple ($V, +, \cdot$), consisting of a set $V$, a map (addition):$$
> 		 \begin{aligned}
> 		  + : V \times V &\to V\\
> 		 (x,y) &\to x + y
> 		 \end{aligned}
> 		$$
> 	 and a map (scalar multiplication):$$
> 		 \begin{aligned}
> 		  + : \mathbb{F} \times V &\to V\\
> 		 (\lambda,x) &\to \lambda x
> 		 \end{aligned}
> 	 $$
> 	is called a real vector space if the following axioms hold for map $\cdot$ and $+$
> 		For all $x,y,z \in \mathbb{F}^n$ and $\lambda, \mu \in \mathbb{R}$ we have
> 			1. $(x + y) + z = x + (y + z)$
> 			2. $x +y = y + x$
> 			3. $x + 0 = x$
> 			4. $x + (-x) = 0$
> 			5. $\lambda (\mu x) = (\lambda \mu)x$
> 			6. $1x = x$
> 			7. $\lambda(x + y) = \lambda x + \lambda y$
> 			8. $(\lambda + \mu)x = \lambda x + \mu x$
> 		

*Note:* $0$ and $1$ don't need to be the value $0$ and $1$ in $\mathbb{R}$, we can understand their role as the null element ($0$) and the unit element ($1$) that only need to satisfy those above axioms.

> [!Definition] Definition 2
> **(Vector subspaces):**  A subset $U$ of $V$ is a subspace of $V$ if and only if $U$ satisfies the following three conditions 
> - $0 \in U$
> - $u,w \in U$ implies $u + w \in U$
> - $a \in \mathbb{F}$ and $u \in U$ implies $au \in U$

> [!Definition] Definition 3
>  **(Sum of subspaces):** Suppose $V_1, V_2,\dots, V_m$ are subspaces of $V$. The sum of subspaces is denoted by
> $$
> 	V_1 + V_2 + \dots + V_m = \{ v_1 + v_2 + \dots + v_m : v_1 \in V_1,\dots, v_m \in V_m\}
> $$

> [!theorem]+ 🧠 Theorem 1
> Suppose $V_1, V_2, \dots, V_m$ are subspaces of $V$.  
> Then $V_1 + \dots + V_m$ is the smallest subspace of $V$ containing $V_1, \dots, V_m$.

> [!Proof]- 🖋 Proof
> Because $0$ is in $V_1,\dots,V_m$, and subspaces are closed under addition, we get $0 + 0 +\dots + 0 = 0 \in V_1+V_2+\dots +V_m$. Then if $x$ is in any $V_i$ we can always put $0 + \dots + x + 0 + \dots = x \in V_1 + V_2 + \dots + V_m$
> Therefore, $V_1, V_2 + \dots + V_m \in V_1 + V_2 + \dots + V_m$. Now we want to prove that it's the smallest subspace. Suppost that there is a subspace of $V$, namely $u$ which containing $V_1,\dots,V_m$ and $U \subset V_1 + V_2 + \dots + V_m$. Let $x$ be a vector such that $x \in V_1 + V_2 + \dots + V_m$ but not in $u$. For all $i$, there exists an $v_i \in V_i$ such that
> $$
> 	u = v_1 + \dots + v_m
> $$
> And since $U$ contains $V_1, V_2, \dots, V_m$ then
> $$
> 	\begin{aligned}
> 			v_1 + v_2 &\in U\\
> 			(v_1 + v_2) + v_3 &\in U\\
> 			&\dots\\
> 			(v_1 + v_2 + \dots + v_{n - 1}) + v_n &\in U\\
> 	\end{aligned}
> $$
> Hence, $u \in U$, which contradicts our assumption that $x$ is not in $U$. Therefore $V_1 + \dots + V_m$ is the smallest subspace of $V$ containing $V_1, \dots, V_m$. $\square$ 
> 
 

> [!NOTE] Definition 4: 
> **(Direct sum, $\oplus$):** Suppose that $V_1, \dots,V_m$ are subspaces of $V$,
> - The sum $V_1 + \dots + V_m$ is called a *direct sum* if each element of $V_1 + \dots + V_m$ can be written in only one way as a sum $v_1  + \dots + v_m$ where each $v_k \in V_k$
> -  If $V_1 + \dots + V_m$ is a direct sum , then $V_1 \oplus \dots \oplus V_m$ denotes $V_1 + \dots + V_m$ 

*Note:* The definition of direct sum requires every vector in the sum to have a unique representation as an appropriate sum.

> [!Theorem] 🧠 Theorem 2:
> Suppose $V_1,\dots, V_m$ are subspaces of $V$. Then $V_1 + V_2 + \dots + V_m$ is a direct sum if and only if the only way to write $0$ as a sum $v_1 + \dots + v_m$, where each $v_k \in V_k$ is by taking each each $v_k$ equal to $0$.  


> [!Proof]- 🖋 Proof
> It suffices to prove the converse, that is if 
> $$
> 	v_1 + v_2 + \dots + v_m = 0
> $$
> then $v_i = 0$, where each $v_i \in V_i$. Now we suppose that there is an element in the sum can be written in two different ways. Suppose that a vector $v$ can be written as
> $$
> v = x_1 + \dots + x_m = y_m + \dots + y_m
> $$
> where each $x_i,y_i \in V_i$. By subtracting the two expressions we get
> $$
> 	(x_1 - y_1) +\dots + (y_1 -y_m) = 0
> $$
> Let $v_i = (x_i - y_i)$ we get $v_1 + \dots + v_m = 0$. By the hypothesis, this implies $v_i$ must be equal to zero, which means $x_i = y_i$ for all $i$, This contradicts the assumption that the representations are distinct, that is $(x_1,\dots,x_m)$ is different from $(y_1,\dots,y_m)$
> 
> Therefore, every element in $V_1 + \dots + V_m$ has a unique representation. Hence, $V_1 +\dots + V_m$ is a direct sum $\square$. 

> [!Theorem 3] 🧠 Theorem 3
> Suppose $U$ and $W$ are subspaces of $V$. Then
> $$
> U + W \text{ is a direct sum } \Leftrightarrow U \cap W = \{0\} 
> $$

> [!Proof]- Proof
> We begin by proving the forward direction, then proceed to the converse.
> Suppose first that $U + W$ is a direct sum and $x$ is a non-zero element such that $x \in U \cap W$ and $x \in U \oplus W$. 
> According to the properties of direct sum, there exists a unique pair $(u,w)$ with$u \in U$ and $w \in W$ such that
> $$
> x = u + w$$
> Using the properties of vector subspaces, we have
> $x, u \in U$ implies $x - u = w \in U$.
> $x,w \in W$ implies $x - w = u \in W$. 
> $x, w\in U$ implies $x +u = u + w + w \in U$ 
> However, $x$ can be rewritten as
> $$x = (u + w +w) - u$$
> for $u + w + w \in U$ and $-u \in W$. This contradicts the assumption that the representations are distinct. Hence,  $x = 0$ and $U \cap W = \{0\}$
> Secondly, suppose that $U \cap W = \{0\}$ and $x \in U + W$ such that $x$ can be written as
> $$x = x_1+ y_1 = x_2 + y_2$$
> which $(x_1,y_1) \neq (x_2,y_2)$ and $x_1, x_2 \in U$, $y_1, y_2 \in W$.  Notice that we have
> $x_1, x_2$ implies $x_1 - x_2 \in U$ 
> $y_1, y_2$ implies $y_2 - y_1 \in W$ 
> By subtracting the two above expression we get
> $$
> 0 = x - x = (x_1 - x_2) + (y_2 - y_1)
> $$
> This implies $x_1 - x_2 = y_2 - y_1 = t$, which means $t \in U$ and $t \in W$, or $t \in U \cap W$.
> However, $0$ is the only element that belongs to $U \cap W$, then $t = 0$ and in particular $x_1 = x_2$ and $y_1 = y_2$ implies $(x_1,y_1) = (x_2,y_2)$, this contradicts the hypothesis that $(x_1,y_1) \neq (x_2,y_2)$. Hence, every element in $U + W$ can only be writen as a unique representation, which means $U+W$ is a direct sum . $\square$ 


# 2 - Finite-Dimensional Vector Spaces
- A linear combination of a list $v_1, \dots,v_m$ of vector in $V$ is a vector of the form
$$
a_1v_1 + \dots + a_mv_m
$$
- Set of all linear combinations of a list of vectors is called
	$$
		span(v_1 + \dots +v_m) = \{a_1v_1 + \dots + a_mv_m: a_1,\dots a_m \in \mathbb{F}\}
	$$
- The span of a list of vectors in $V$ is the smallest subspace of $V$ containing all vectors in the list
- If $span(v_1, \dots, v_m) = V$ we say that list spans $V$. 
- a list of vectors in $V$ is called linearly independent if the only choice of $a_1,\dots,a_m \in \mathbb{F}$ that makes
$$
a_1v_1 + \dots a_m v_m = 0
$$
    is $a_1 = \dots = a_m = 0$. 

> [!NOTE] Lemma
> Suppose $v_1,\dots,v_m$ is a linearly dependent list in $V$. Then there exists $k \in \{1,\dots,m\}$ such that
> $$
> v_k \in span(v_1,\dots,v_k)$$
> Furthermore, if $k$ satisfies the condition above and the $k^{th}$ term is removed from $v_1,\dots,v_m$ then the span of remaning list equals $span(v_1,\dots,v_m)$  

> [!NOTE] Theorem 1
In a finite-dimensional vector space, the length of every linearly independent list of vectors if less than or equal to the length of every spanning list of vectors

> [!Proof]- Proof
> Proof: Let $A = (v_1, \dots, v_m)$ be a linearly independent list, and let $B = (w_1, \dots, w_n)$ be a spanning list of $V$. We aim to prove that $m \leq n$.
> 
> Since $B$ spans $V$, each $v_i$ can be written as a linear combination of vectors from $B$. In particular, $v_1$ is a linear combination of $w_1, \dots, w_n$. Therefore, the list $(v_1, w_1, \dots, w_n)$ is linearly dependent.
> 
> Because $A$ is linearly independent, $v_1 \neq 0$. Hence, there must exist some $k > 0$ such that $w_k$ is a linear combination of $v_1, w_1, \dots, w_{k-1}$. Removing $w_k$ from $B$, we still have a spanning list.
> 
> We continue this process: successively add each $v_i$ into the list and eliminate one redundant vector in $B$ each time to maintain a spanning list. Eventually, we obtain a list containing all of $v_1, \dots, v_m$ and still spanning $V$. Since we remove one vector from $B$ for each $v_i$ added, we cannot perform this more than $n$ times. Therefore, $m \leq n$.

> [!NOTE] Theorem 2
> Every subspace of a finite-dimensional vector space is finite-dimensional.

> [!Proof]- Proof
> Let $V$ be a finite-dimensional vector space, and let $U \subseteq V$ be a subspace.  
> We aim to show that $U$ is finite-dimensional.
> 
> If $U = \{0\}$, then $U$ is clearly finite-dimensional.  
> Otherwise, there exists a nonzero vector $u_1 \in U$.  
> Let $A = \{u_1\}$.
> 
> Proceed inductively: suppose we have constructed a linearly independent list $A = \{u_1, u_2, \dots, u_{k-1}\} \subseteq U$.  
> If $U \subseteq \mathrm{span}(A)$, then $U$ is spanned by finitely many vectors, and we are done.
> 
> Otherwise, there exists $u_k \in U$ such that  
> $$
> u_k \notin \mathrm{span}(u_1, u_2, \dots, u_{k-1}).
> $$  
> Add $u_k$ to $A$ and repeat the process.
> 
> Since $V$ is finite-dimensional, any linearly independent set in $V$ contains at most $\dim V$ vectors.  
> Therefore, this process must terminate after finitely many steps.  
> At termination, we have a finite linearly independent set $A \subseteq U$ such that $U \subseteq \mathrm{span}(A)$,  
> i.e., $U = \mathrm{span}(A)$.
> 
> Hence, $U$ is finite-dimensional. $\square$

 -  A basis of 𝑉 is a list of vectors in 𝑉 that is linearly independent and spans 𝑉.
 - A list of vectors $v_1,\dots,v_m$ in $V$ is a basis of $V$ if and only if every $v \in V$ can be written uniquely in the form
 $$
	 v = a_1v_1 + \dots a_mv_m
 $$
 - Every spanning list in a vector space can be reduced to a basis of the vector space.
 - Every finite-dimensional vector space has a basis.
 - Every linearly independent list of vectors in a finite-dimensional vector space can be extended to a basis of the vector space.