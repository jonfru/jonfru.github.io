---
title: Virtual homological torsion in graphs of free groups with cyclic edge groups
layout: page
---

<script>
  window.MathJax = {
    tex: {
      inlineMath: [['$', '$'], ['\\(', '\\)']],
      displayMath: [['$$', '$$'], ['\\[', '\\]']]
    }
  };
</script>
<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>


# **Virtual homological torsion in graphs of free groups with cyclic edge groups** *(j/w [Dario Ascari](https://sites.google.com/view/dario-ascari))*
#### Extended abstract to accompany a poster presented at the William Rowan Hamilton Geometry and Topology Workshop, celebrating Martin Bridson’s 60th birthday

---
In 2013, Hongbin Sun proved that homological torsion is remarkably abundant in finite covers of closed hyperbolic 3-manifolds. Specifically, given a closed, hyperbolic 3-manifold $M$, for every finite abelian group $A$ there exists a finite cover $M’_A$ of $M$ such that $A$ appears as a direct summand of $H_1(M'_A)$. Groves and Chu later extended this result to most finite-volume hyperbolic 3-manifolds with empty or toroidal boundary.

While these results stop short of proving the exponential torsion growth conjecture, they show that the geometry of $M$ can be leveraged to produce a wide range of torsion in the homology of its finite covers. The core of the argument involves immersing 2-complexes $X_p$ with $H_1(X_p) = \mathbb{Z}^n \oplus \mathbb{Z}/p\mathbb{Z}$—essentially surfaces with boundary, modified by attaching a $p$-th root of the boundary loops—into $M$, combining them via a ping-pong construction, and then pushing their homology into that of a finite cover via a virtual retraction.

In this project, we investigate whether analogous torsion phenomena arise in a different context: hyperbolic groups that split as graphs of free groups with cyclic edge groups. This class often mirrors behavior found in 3-manifold topology, and here too, we find a strong analogue:

>**Theorem:** Let $G$ be a hyperbolic group that splits as a graph of free groups with cyclic edge groups, and that is not isomorphic to a free product of free and surface groups. Then for every finite abelian group $M$, there exists a finite-index subgroup $H \le  G$ such that $M$ is a direct summand of the abelianization $H^{ab}$ of $H$.

test case - branched surfaces - add table for the picture

start with "triple branched surface" - three surfaces, each with $b$ boundary components, glued together like in the picture. 

>**Example** $b=2$, we choose $\mathbb{Z}/2 \mathbb{Z} \oplus \mathbb{Z} / 3\mathbb{Z}$. we do bla bla bla


Then start with Wilton - metnion Wilton and Calegari - and say that there are surfaces immersing etc which allow us to build a precover (space that can be completed to a finite-sheeted cover) that does what we want.
>**Theorem:** [Wilton]...

then philosophy about Wilton - not free means... Then say not a free product of free and surface groups - manifests in one of two ways

1) there are 3 things glued together - add a picture. In this case, up to some acrobatics with finite covers etc, it's easy to get the result (add picture again).
2) there is a rigid vertex.

If we are in case 2 (and not case 1), things are trickier. For this we embed two different surfaces within a rigid vertex, and use them to mimic branching. We call such a piece "artificial branching". -- Here should probably say something about Wilton's rigid theorem...

Suppose that the two surfaces were embedded - intersecting only at the boundaries. Then we are exactly at the previous case. In general, this gives us an obvious map from a branched surface to our group - replace the rigid vertex with $S_1 \sqcup S_2$. A key observation here is that in order to obtain an injective map on the torsion part of the abelianization, all that we need is that if $b_1,\ldots,b_k$ are the boundaries shared between the surfaces, then $[b_1],\ldots,[b_k]$ generate a rank-$k$ direct summand in the abelianization of $H$ (the rigid vertex).

To obtain that we use a minimality argument, which crucially relies on Calegari's proof that *stable commutator length* is rational in free groups. The precise form of the theorem that we use is the following:
>**Theorem:** [Calegari]...

Then give a short explanation of minimality.

Seal the deal by saying that we can now use an artificial branching piece as in the branched surface case
