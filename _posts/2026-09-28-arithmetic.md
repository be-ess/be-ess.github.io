---
title: "Notes on Serre's <cite>Arithmetic</cite>"
pithy: "Tackling a GTM."
---

For [an upcoming summer
project](https://ms.unimelb.edu.au/engage/vacation-scholarships), I'm reading a
few books, the first of which is *A Course in Arithmetic* by Jean-Pierre Serre,
who recently turned 100 and is still doing mathematics! The book is an early
entry (vol. 7, 1973) in the
[(in)](https://aperiodical.com/2022/05/didnt-graduate-texts-in-mathematics/)famous
*Graduate Texts in Mathematics* series from the Springer-Verlag. It's short, at
just 113 pages, and surprisingly readable. The university's copy, acquired over
50 years ago, is pretty beaten up. It's clearly not too popular, though: I had
to request it from storage.

I was charmed by the final paragraph of the preface:

> The two parts correspond to lectures given in 1962 and 1964 to second year[^1]
> students at the Ecole Normale Supérieure. A redaction of these lectures in the
> form of duplicated notes, was made by J.-J. Sansuc (Chapters I–IV) and J.-P.
> Ramis and G. Ruget (Chapter VI–VII). They were very useful to me; I extend
> here my gratitude to their authors.

Is it normal to teach a class without one's own prepared notes? Maybe that's
reserved for heavy hitters like Serre.

I'm particularly interested in the second (analytic, rather than purely
algebraic) part, so let's begin with chapter VI.

## The Theorem on Analytic Progressions

The goal of this chapter is to work up to a proof of the [Dirichlet's theorem on
arithmetic
progressions](https://en.wikipedia.org/wiki/Dirichlet%27s_theorem_on_arithmetic_progressions),
which states that for any pair of coprime positive integers $$a$$ and $$m$$,
there exist infinitely many primes $$p$$ with $$p \equiv a \ (mod m)$$.

We start out by thinking about a finite abelian group $$G$$ along with its
characters—homomorphisms from $$G$$ to $$\mathbf{C}^\times$$—which form the dual
group $$\widehat G$$.[^2] It's straightforward enough that to discuss it all here
would amount to a poor retelling of the book, but I really like the lovely
simple proof of proposition 4.

> **Proposition 4.**—Let $$n = Card(G)$$ and let $$\chi \in \widehat G$$.
>
> $$ \sum_{x\in G} \chi(x) = \begin{cases} n & \text{if}\, \chi = 1,\\ 0 &
> \text{if}\, x \ne 1. \end{cases} $$

Indeed, "the first formula is obvious." For the latter, here's an illustration
for $$G \cong \mathbf{Z}/3\mathbf{Z}$$.

![Two complex planes. The first shows the third roots of unity, with arrows from
the origin to each. The second shows the same arrows shifted to form a closed
triangle returning to the origin.](/images/arithmetic/symmetry.svg)

Thinking about the geometric argument, it's clear that the proof will exploit
the symmetry of the setup. Just pick a $$y \in G$$ such that $$\chi(y) \ne 1$$
and notice that

$$ \chi(y) \sum_{x \in G} \chi(x) = \sum_{x \in G} \chi(x y) = \sum_{x\in G}
\chi(x). $$

But since $$\chi(y) \ne 1$$, it must be the case that $$\sum_{x\in G}\chi(x) =
0$$. How elegant! Geometrically, I think of this as moving each image
$$\chi(x)$$ around by multiplying by $$\chi(y)$$. This operation has to be
bijective because $$G$$ is a group and $$\chi$$ a homomorphism, so the sum of
all the points must not have changed under this operation. Equally, the sum of
the points must also have been multiplied by $$\chi(y)$$. So it must've been
zero all along.

*More to come. Comments, questions, or chat welcome. You can email me at
`benstankovich23@gmail.com`.*

<hr>

[^1]: I thought it surprising that such a course would be taught to second-year
    students, but the ENS (and other *grandes écoles*) appear to require [two
    years of prior
    study](https://en.wikipedia.org/wiki/Classe_pr%C3%A9paratoire_aux_grandes_%C3%A9coles)
    before admission, so it's a bit less impressive than it sounds at first.

[^2]: Yes, it bothers me that the $$\widehat G$$ bumps the line spacing.
