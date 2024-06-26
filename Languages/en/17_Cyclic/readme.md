For any element $g \in G$, $g^n = e$, where $n$ is the order of $g$. Since $G$ is a cyclic group generated by $g$, all the elements in $G$ can be expressed as powers of $g$, i.e., $G = \{g^0, g^1, g^2, ..., g^{n-1}\}$. Therefore, $|G| = n$.

**Necessity**

If $|G| = n$, we can prove that the order of the generator $g$ is also $n$. Since $g^n = e$, the order of $g$ must be at most $n$. If the order of $g$ is less than $n$, then there exists an element $g^k$ such that $k < n$ and $g^k = e$. However, this contradicts the fact that $G$ is generated by $g$ and all the elements in $G$ can be expressed as powers of $g$. Therefore, the order of $g$ can only be $n$.
**Group Homomorphism:** For any $a, b \in \mathbb{Z}$, it holds that $f(a + b) = g^{a+b} = g^ag^b = f(a)f(b)$. Therefore, $f$ is a group homomorphism.

**Surjective Homomorphism:** The image of the homomorphism $\{f(a) | a \in Z_n\} = \{g^a | a \in Z_n\} = \left \langle \, g \, \right \rangle$. So, the image of the homomorphism is equal to the group $G$, and $f$ is a surjective homomorphism.

**Injective Homomorphism:** The order of the generator $g$ of group $G$ is $n$, so we have $g^{kn} = e_G$, where $k$ is an integer. Therefore, the kernel of the homomorphism $\text{ker}(f)= \{kn \mod n| k \in Z\}=\{0\}$, which is the identity element of $Z_n$. According to the necessary and sufficient conditions for injective homomorphism, $f$ is an injective homomorphism.

Since the group homomorphism $f$ is both surjective and injective, any finite cyclic group $G$ of order $n$ is isomorphic to the additive group $Z_n$ of integers modulo $n$. Proof is complete.

</details>

Therefore, for any cyclic group $G$, it is isomorphic either to the additive group $Z_n$ of integers modulo $n$ or to the group of integers $Z$. Isomorphism represents that two groups have the same structure, which means that the properties of $Z_n$ or $Z$ that we introduced earlier can be transferred to any cyclic group.

## 4. Review of Euler's theorem

In the foundation of number theory, we introduced Euler's theorem, connecting the properties of Euler's function and the cyclic property of the multiplicative group modulo n.

**Euler's theorem:** If the integer $a$ and the positive integer $n$ are coprime (i.e., $\gcd(a,n)=1$), then $a^{\phi(n)} \equiv 1 \pmod{n}$.

Now let's prove it using the properties of cyclic groups.

First, consider the multiplicative group modulo n, denoted as $Z^* _n$, whose order is $\phi(n)$. Suppose the integer $a$ is coprime with $n$, that is, $\gcd(a,n)= 1$, we have $a \equiv 1 \mod n$, so $a \in Z^* _n$. We can construct a cyclic group $A$ with $a$ as the generator, then $A$ is a subgroup of $Z^* _n$. Let the order of group $A$ be $k$, then $a^k \equiv 1 \pmod{n}$. According to Lagrange's theorem, the order of subgroup $A$ divides the order of $Z^* _n$, that is, $k | \phi(n)$. In other words, there exists an integer $q$ such that $\phi(n) = kq$. We have:

$$
a^{\phi(n)} = a^{kq} = (a^k)^q = 1^q = 1 \pmod{n}
$$

That is, $a^{\phi(n)} \equiv 1 \pmod{n}$, and the proof is complete.

## 5. Summary

In this lesson, we introduced cyclic groups, which have a simple structure and can be generated by a single element (generator). All cyclic groups are Abel groups, and subgroups and quotient groups of cyclic groups are also cyclic groups. The order of cyclic groups and the order of elements have a special relationship. There are many properties, so it is recommended to review them several times to become familiar with them. Any infinite cyclic group is isomorphic to $Z$, and any finite cyclic group is isomorphic to $Z_n$.
According to the definition, the cyclic group G is generated by g. If the order of G is n, the group G =  <g> = {e, g, ..., g^(n-1)} contains n distinct elements, so the order of the element g is n.

**Necessity**

According to the definition, the cyclic group G is generated by g. If the order of g is n, the group G =  <g> = {e, g, ..., g^(n-1)} contains n distinct elements, so the order of the group G is n.

</details>

In the integer modulo 5 multiplication group (Z*_5, ×), the order of the generator 2 or 3 is 4, and the order of the group is also 4.

**3. If G is an n-order cyclic group and d is a positive integer that divides n, then G has a unique d-order subgroup.**

<details><summary>Click to expand proof👀</summary>

First, we prove the existence of a d-order subgroup. Since the order of the cyclic group G is n and d is a positive integer that divides n, we can use g^(n/d) as the generator to generate the cyclic group <g^(n/d)> = {e, g^(n/d), g^(2n/d),..., g^(n-n/d)}, which has an order of d. Therefore, a d-order subgroup exists.

Next, we prove the uniqueness of the d-order subgroup. Using proof by contradiction, assume that there exists another d-order cyclic subgroup <g^(k)> in the group G, where k is an element of Z. According to the definition of order, (g^(k))^d = g^(kd) = e. According to the property of order, n divides kd, which means n/d divides k. Therefore, according to the property of Abel groups, <g^(k)> is a subgroup of <g^(n/d)>. Since they both have an order of d, they are the same cyclic group <g^(n/d)>. Therefore, the d-order subgroup is unique.

</details>

The order of the integer modulo 6 addition group (Z_6) is 6, so it has 4 subgroups with orders of 1, 2, 3, 6, which are {0}, {0,3}, {0,2,4}, and {0,1,2,3,4,5}, respectively.

The order of the integer modulo 5 multiplication group (Z^*_5) is 4, so it has 3 subgroups with orders of 1, 2, 4, which are {1}, {1, 4}, and {1,2,3,4}, respectively.

**4. The order of the element g^k in an n-order cyclic group <g> is n/gcd(n,k).**

<details><summary>Click to expand proof👀</summary>

Assume that the order of the element g^k is m, according to the definition of order, m is the smallest positive integer that satisfies (g^k)^m = e. According to the property of order, n divides km, which can be simplified to m congruent to 0 modulo (n/gcd(n,k)). The smallest positive integer that satisfies this condition is m = n/gcd(n,k). Therefore, the order of the element g^k is n/gcd(n,k). Proof complete.

</details>

The order of the integer modulo 6 addition group (Z_6) is 6. The element 2 = 1 + 1 = 1^2 has an order of 3, the element 3 = 1 + 1 +1 = 1^3 has an order of 2, the element 4 = 1^4 has an order of 3, and the element 5 = 1^5 has an order of 6.

The order of the integer modulo 5 multiplication group (Z^*_5) is 4. The element 2 = 2^1 has an order of 4, the element 3 = 2^3 has an order of 4, the element 4 = 2^2 has an order of 2, and the element 1 = 2^4 has an order of 1.

**5. An n-order cyclic group has phi(n) generators.**

<details><summary>Click to expand proof👀</summary>

According to the previous property, only when gcd(n, k) = 1, the order of the element g^k is n, which means it is a generator. According to Euler's totient function, there are phi(n) integers less than n and coprime to n. In other words, there are phi(n) values of k that make g^k a generator. Therefore, an n-order cyclic group has phi(n) generators. Proof complete.

</details>

The order of the integer modulo 6 addition group (Z_6) is 6, so it has phi(6) = phi(2) * phi(3) = 1 * 2 = 2 generators, which are 1 and 5.

The order of the integer modulo 5 multiplication group (Z^*_5) is 4, so it has phi(4) = phi(2^2) = 2^2 - 2 = 2 generators, which are 2 and 3.

**6. The order of an element in an n-order finite group G is a factor of n.**

<details><summary>Click to expand proof👀</summary>

Let a be an element in group G. According to Lagrange's theorem, the order of a subgroup divides the order of an element. Therefore, |<a>| divides |G|. Also, since |G| = n and |a| = |<a>|, the order of an element is a factor of n. Proof complete.

</details>

The order of the integer modulo 6 addition group (Z_6) is 6. The element 2 has an order of 3, which is a factor of 6.

The order of the integer modulo 5 multiplication group (Z^*_5) is 4. The element 4 has an order of 2, which is a factor of 4.

**7. If p is a prime number, then the integer modulo p multiplication group Z^*_p has phi(p-1) generators.**

<details><summary>Click to expand proof👀</summary>

First, we need to determine the order of Z^*_p, which contains phi(p) elements. Since p is a prime number, phi(p) = p-1, so the order of Z^*_p is p-1. According to property 5, Z^*_p has phi(p-1) generators. Proof complete.

</details>

5 is a prime number, so Z^*_5 has phi(4) = phi(2^2) = 2^2 - 2^1 = 2 generators, which are 2 and 3.

## 3. Isomorphism of Cyclic Groups

In this section, we introduce the isomorphism of cyclic groups. Cyclic groups are the simplest type of groups and can be classified into two categories, one is isomorphic to Z and the other is isomorphic to Z_n. Therefore, when studying the properties of cyclic groups, we can study the simpler Z or Z_n.

**1. Any infinite cyclic group is isomorphic to the integer addition group Z.**

<details><summary>Click to expand proof👀</summary>

Let G be an infinite cyclic group generated by g. Let the mapping f: Z -> G be defined as f(x) = g^x.

**Group homomorphism:** For any a, b in Z, we have f(a + b) = g^(a+b) = g^a * g^b = f(a) * f(b). Therefore, f is a group homomorphism.

**Surjective homomorphism:** The image of the homomorphism, {f(a) | a in Z} = {g^a | a in Z} = <g>, is equal to the group G. Therefore, the homomorphism f is surjective.

**Injective homomorphism:** Since the infinite cyclic group has an infinite order, there is only g^0 = e_G. Therefore, the kernel of the homomorphism, ker(f) = 0. According to the condition of injective homomorphism, f is an injective homomorphism.

The group homomorphism f is both surjective and injective, therefore the infinite cyclic group G is isomorphic to the integer addition group Z. Proof complete.

</details>

**2. Any n-order finite cyclic group is isomorphic to the integer modulo n addition group Z_n.**

<details><summary>Click to expand proof👀</summary>

Let G be an n-order finite cyclic group G = <g> = {g^a | a in Z_n}. Let the mapping f: Z_n -> G be defined as f(x) = g^x.

**Group homomorphism:** For any a, b in Z_n, we have f(a + b) = g^(a+b) = g^a * g^b = f(a) * f(b). Therefore, f is a group homomorphism.

**Surjective homomorphism:** The image of the homomorphism, {f(a) | a in Z_n} = {g^a | a in Z_n} = <g>, is equal to the group G. Therefore, the homomorphism f is surjective.

**Injective homomorphism:** The n-order finite cyclic group has n elements. Therefore, there are n distinct powers of g. Therefore, the homomorphism is injective.

The group homomorphism f is both surjective and injective, therefore the n-order finite cyclic group G is isomorphic to the integer modulo n addition group Z_n. Proof complete.

</details>