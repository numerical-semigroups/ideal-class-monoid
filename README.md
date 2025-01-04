# Ideal class monoid of a numerical semigroup
In this repository we present the tools needed to develop the examples in the papers 
  - L. Casabella, M. D'Anna, P. A. García-Sánchez, Apéry sets and the ideal class monoid of a numerical semigroup, [Mediterr. J. Math. 21:7 (2024)](https://link.springer.com/article/10.1007/s00009-023-02550-8); [arxiv.org/2302.09647](https://arxiv.org/abs/2302.09647),
  - P. A. García-Sánchez, The isomorphism problem for ideal class monoids of numerical semigroups, [Semigroup Forum (2024)](https://doi.org/10.1007/s00233-024-10429-7), [arXiv:2311.15265](https://arxiv.org/abs/2311.15265).
  - S. Bonzio, P. A. García-Sánchez, The poset of normalized ideals of numerical semigroups with multiplicity three, [arXiv:2407.21697](https://arxiv.org/abs/2407.21697).
  - S. Bonzio, P. A. García-Sánchez, When the poset of the ideal class monoid of a numerical semigroup is a lattice, [arXiv:2412.07281](https://arxiv.org/abs/2412.07281).

The notebook [ideal-class-monoid](https://github.com/numerical-semigroups/ideal-class-monoid/blob/main/class-monoid.ipynb) contains the necessary code (written using the [GAP](https://www.gap-system.org/) package [numericalsgps](https://gap-packages.github.io/numericalsgps/)), together with some examples extracted from the first manuscript. The notebook [isomorphism-ideal-class-monoid](https://github.com/numerical-semigroups/ideal-class-monoid/blob/main/isomorphism-ideal-class-monoid.ipynb) contains examples for the second manuscript. The file [poset-normalized-ideal](https://github.com/numerical-semigroups/ideal-class-monoid/blob/main/poset-normalized-ideals.ipynb) contains examples and the code needed for the poset of normalized ideals of a numerical semigroup with multiplicity three, while the file [lattice-normaliced-ideals-ns](https://github.com/numerical-semigroups/ideal-class-monoid/blob/main/lattice-normalized-ideals-ns.ipynb) has computations dealing with when this poset is a lattice.

This [presentation](https://pedritomelenas.github.io/slides-imns-2024) contain slides on this topic at [IMNS2024](https://imns2024.uca.es/).

You can run this repo via [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/numerical-semigroups/ideal-class-monoid/HEAD)

## Apéry sets and the ideal class monoid of a numerical semigroup

Given a Dedekind domain $D$, its class group is defined as the set of fractional ideals of $D$ modulo its principal ideals. The cardinality of the class group measures how far the domain is from being a principal ideal domain. Fractional ideals can be considered on any integral domain. However, on a domain, not every fractional ideal has an inverse, and thus the quotient of the set of fractional ideals modulo principal ideals is no longer a group, and it is just a commutative monoid. In both cases, the operation that gives the group or monoid structure is the product of equivalence classes of fractional ideals, which is defined as the class of the product of any two representatives of the classes.

Inspired by the notion of ideal class group for Dedekind domains, Barucci and Khouja introduced in [1] the concept of ideal class monoid of a numerical semigroup. Recall that a numerical semigroup $S$ is a submonoid of the set of nonnegative integers under addition such that $\mathbb{N}\setminus S$ (known as the set of gaps of $S$) has finitely many elements. A set $I$ of integers is said to be an *ideal* of $S$ if $I+S\subseteq I$ and $I$ has a minimum. The sum of two ideals of $S$ is again an ideal of $S$. If $I$ and $J$ are ideals of $S$, we write $I\sim J$ if there exists an integer $z$ such that $I=z+J$. The *ideal class monoid* of $S$ is defined as the set of ideals of $S$ modulo this relation; the operation considered now is addition of ideals instead of multiplication as in the case of integral domains. It can be easily proven that this monoid is isomorphic to the monoid of ideals of $S$ having its minimum equal to zero.

Barucci and Khouja were mainly interested in the following three problems: find bounds for the cardinality of the ideal class monoid of a numerical semigroup; describe the generators of the ideal class monoid of a numerical semigroup; find properties about the reduction number of the elements of the class group. The reduction number of an ideal $I$ is the minimum positive integer $r$ such that $(r+1)I=rI$. It can be shown that it is invariant under translations, and thus studying the reduction number for each element in the ideal class monoid provides a way to understand how it behaves for every ideal of the semigroup.

Our main goal is not only to sharpen and extend the results obtained by Barucci and Khouja, but also to determine properties of the numerical semigroup from those of its ideal class monoid.

Apart from using anti-chains of gaps to find bounds for the cardinality of the ideal class monoid of a numerical semigroup (that was the main tool used in [1]), we introduce the concept of Kunz coordinates of an ideal of a numerical semigroup. This enables us to find a one-to-one correspondence between the set of elements in the ideal class monoid and the set of integer solutions of a linear system of inequalities. With this we can find new bounds for the cardinality of the ideal class monoid of a numerical semigroup, and we can depict when these bounds are attained.

As a consequence of the relationship between the Apéry set of an ideal and the Apéry set of its ambient semigroup, we fully characterize the canonical ideal of a numerical semigroup from the shape of its Apéry set. As a consequence we prove that the canonical ideal is generated by the the set $\lbrace\mathrm{F}(S)-g : g\in \mathrm{PF}(S)
\rbrace$, with $\mathrm{F}(S)=\max(\mathbb{Z}\setminus S)$, the Frobenius number of $S$, and $\mathrm{PF}(S)=\mathrm{Maximals}_{\le_S}(\mathbb{Z}\setminus S)$, the set of pseudo-Frobenius numbers of $S$. Some progress is also made in the calculation of bounds of the reduction number of ideals whose minimal generators are smaller than the multiplicity of the semigroup.

We also use Kunz coordinates to study the Hasse diagram of the ideal class monoid of a numerical semigroup with respect to inclusion. The minimum element in this diagram is the semigroup itself, while the maximum is $\mathbb{N}$. We describe the set of minimal non-trivial elements, and the set of the maximal elements different from $\mathbb{N}$. The cardinality of the first set is the type of the semigroup, and the cardinality of the latter is the multiplicity of the semigroup minus one. Any maximal strictly ascending chain in this Hasse diagram is precisely the genus of the semigroup plus one. Thus, some of the classical invariants of the numerical semigroup are reflected in the shape of the Hasse diagram of its ideal class monoid with respect to inclusion.

We prove that generators of the ideal class monoid as defined in [1] correspond to irreducible elements (see [2]). We study how irreducible elements, atoms, quarks and prime elements are related in the ideal class monoid of a numerical semigroup. There are numerical semigroup whose ideal class monoid has no atoms. We show that a numerical semigroup is irreducible if and only if its ideal class monoid has at most two quarks (the existence of a single quark translates to the symmetry of the semigroup). The set of unitary extensions of a numerical semigroup is the set of idempotent quarks of the ideal class monoid of the semigroup.

At the end of [3], we propose a series of open questions related to the ideal class monoid of a numerical semigroup, which together with the results presented so far highlight the potential relevance that the study of ideal class monoids might have not only in the study of numerical semigroups, but also in a better understanding of non-unique factorization invariants on a non-cancellative setting. The circle closes, since the initial motivation of the study of the ideal class group of a Dedekind monoid was precisely to determine the behavior of non-unique factorizations in rings of algebraic integers.

[1] V. Barucci, F. Khouja, On the class semigroup of a numerical semigroup, Semigroup Forum, 92 (2016), 377-392.   

[2] S. Tringali, An Abstract Factorization Theorem and Some Applications,  J. Algebra, 602 (2022), 352--380.

[3] L. Casabella, M. D'Anna, P. A. García-Sánchez, Apéry sets and the ideal class monoid of a numerical semigroup, [Mediterr. J. Math. 21:7 (2024)](https://link.springer.com/article/10.1007/s00009-023-02550-8); [arxiv.org/2302.09647](https://arxiv.org/abs/2302.09647).

[4] P. A. García-Sánchez, The isomorphism problem for ideal class monoids of numerical semigroups, [Semigroup Forum (2024)](https://doi.org/10.1007/s00233-024-10429-7); [arXiv:2311.15265](https://arxiv.org/abs/2311.15265).

