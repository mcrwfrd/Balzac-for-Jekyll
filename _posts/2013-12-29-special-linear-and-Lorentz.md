---
layout: post-light-feature
title: Relationships between the special linear group and the Lorentz group
description: "We’ll introduce both the 2 x 2 special linear group and the Lorentz group. We'll also show some close relationships between between these two groups which have important physical implications."
categories: articles
date: 2013-12-29
image: 
        feature: soft-trees.jpg
published: false
---

### The $$ 2 \times 2 $$ Special Linear Group

Consider the set of $$ 2 \times 2 $$ matrices of determinant one with complex entries, denoted $$ SL(2, \mathbb{C}) $$. We claim that this set forms a group under standard matrix multiplication. The $$ 2 \times 2 $$ identity matrix has determinant one and has entries in $$ \mathbb{R} \subseteq \mathbb{C} $$, so this is clearly the required identity element for this set. To show that each element $$ A \in SL(2, \mathbb{C}) $$ has an inverse element, it suffices to recall that 
$$ 
\det A^{-1} = \frac{1}{\det A} = 1
$$
To see that this set is closed under matrix multiplication, consider two matrices $$ A, B \in SL(2, \mathbb{C}) $$ and recall that 
$$ 
\det A B = \det A \det B = 1 \cdot 1 = 1 
$$
Finally, we already know that standard matrix multiplication is associative. Thus, we conclude that $$ SL(2, \mathbb{C})$$ forms a group under matrix multiplication. 

### The Lorentz Group

The Lorentz group is the group composed of Lorentz transformations under the standard matrix multiplication. What are the Lorentz transformations? In a sentence, we could say that they are those linear transformations on the four-vectors of Minkowski space which preserve the Lorentz metric. But since that definition is a bit of mouthful, let's break it down into chunks. Minkowski space, denoted $$ \mathbb{M} $$, is the usual four-dimensional vector space $$ \mathbb{R}^4 $$ endowed with a particular metric called the Lorentz metric. For any vector $$ A^{\mu} = (A^0, A^1, A^2, A^3) \in \mathbb{M} $$, where the superscripts denote which components we're working with, the Lorentz metric is given by 
$$
||A||^2 = A^0 A^0 - \vec{A} \cdot \vec{A} = A^0 A^0 - A^1 A^1 -A^2 A^2 -A^3 A^3
$$
Notice that we're using tensor notation here. This is a convenient way to go about things since our metric has a few nasty minus signs in it. We can deal with these in an elegant fashion by introducing the following subscript notation:
$$ 
A_0 = A^0 \quad \text{and} \quad A_i = -A^i \quad \text{for} \quad i = 1, 2, 3,
$$
so that 
$$
\begin{align}
||A||^2 &= A^0 A^0 - A^1A^1 - A^2 A^2 - A^3 A^3 \newline
&= A^0 A_0 + A^1 A_1 + A^2 A_2 + A^3 A_3  \newline
&= A^{\mu} A_{\mu} 
\end{align}
$$
Now, we can make use of this notation in order to translate the idea that the Lorentz transformations preserve the Lorentz metric into something that we can manipulate mathematically. 

After adding a few steps, we can use this notation to see that the Lorentz transformations are really just those linear transformations $$ \Lambda $$ which satisfy the equation 
$$
{\Lambda} ^T G \Lambda = G,
$$
where 
$$ 
G = 
\begin{pmatrix}
1 & 0 & 0 & 0 \newline
0 & -1 & 0 & 0 \newline
0 & 0 & -1 & 0 \newline
0 & 0 & 0 & -1 
\end{pmatrix}
$$ 
which is just the matrix associated with the metric tensor $$ g_{\mu \nu} $$.

Now, we will use this new definition of the Lorentz transformations to show that the set of all Lorentz transformations, denoted $$ L $$ forms a group with standard matrix multiplication as their binary operation. First, we need to show that $$L$$ has an identity element. The natural choice is the $$ 4 \times 4 $$ identity matrix, $$ I_4 $$. To see that $$ I_4 \in L $$, simply observe that 
$$
I ^T G I = I G I = I G = G.
$$
The next step is to show that each $$ \Lambda \in L $$ has its own inverse element which is itself a member of $$ L $$. We first show that such an inverse exists. Since $$ \Lambda \in L $$, we know that $$ {\Lambda} ^T G  \Lambda = G $$. Taking the determinant of both sides, we quickly see that 
$$
-1 = \det G = \det {\Lambda}^T G \Lambda = - \det {\Lambda} ^T \det \Lambda = - \left( \det \Lambda \right) ^2. 
$$
From this statement, we can conclude that the determinant of any $$ \Lambda \in L $$ must be non-zero, and thus has an inverse element. To show that this inverse element is in $$ L $$, we again start with $$ {\Lambda} ^T G \Lambda = G $$. Left-multiplying both sides of this equation by $$ \left( {\Lambda}^{-1} \right) ^T $$ and right-multiplying by $$ {\Lambda}^{-1} $$ gives us 
$$
\left( {\Lambda}^{-1} \right) ^T G {\Lambda}^{-1} =  \left( {\Lambda}^{-1} \right) ^T {\Lambda} ^T G \Lambda {\Lambda}^{-1} = \left( \Lambda {\Lambda}^{-1} \right)^T G ( \Lambda {\Lambda}^{-1} ) = G
$$
To show the closure of $$ L $$, consider $$ \Lambda, \Gamma \in L$$ and observe that 
$$
(\Lambda \Gamma)^T G \Lambda \Gamma = \Gamma^T \Lambda^T G \Lambda \Gamma = \Gamma^T G \Gamma = G.
$$
Finally, combining identity, inverse and closure with the fact that matrix multiplication is associative, we can conclude that the Lorentz transformations form a group.




### The Homomorphism

###The Isomorphism
