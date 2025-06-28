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
### Background

In 2013, Hongbin Sun proved that homological torsion is remarkably abundant in finite covers of closed hyperbolic 3-manifolds. Specifically, given a closed, hyperbolic 3-manifold $M$, for every finite abelian group $A$ there exists a finite cover $M’_A$ of $M$ such that $A$ appears as a direct summand of $H_1(M'_A)$. Groves and Chu later extended this result to most finite-volume hyperbolic 3-manifolds with empty or toroidal boundary.

While these results stop short of proving the exponential torsion growth conjecture, they show that the geometry of $M$ can be leveraged to produce a wide range of torsion in the homology of its finite covers. The core of the argument involves immersing 2-complexes $X_p$ with $H_1(X_p) = \mathbb{Z}^n \oplus \mathbb{Z}/p\mathbb{Z}$—essentially surfaces with boundary, modified by attaching a $p$-th root of the boundary loops—into $M$, combining them via a ping-pong argument, and then pushing their homology into that of a finite cover via a virtual retraction.
<div align="center">
  <img src="Xp.png" style="max-width: 100%; width: 400px;" />
</div>
In this project, we investigate whether analogous torsion phenomena arise in a different context: hyperbolic groups that split as graphs of free groups with cyclic edge groups. This class often mirrors behavior found in 3-manifold topology, and here too, we find a strong analogue:

>**Theorem:** Let $G$ be a hyperbolic group that splits as a graph of free groups with cyclic edge groups, and that is not isomorphic to a free product of free and surface groups. Then for every finite abelian group $M$, there exists a finite-index subgroup $H \le  G$ such that $M$ is a direct summand of the abelianization $H^{ab}$ of $H.$

---
### Branched surfaces and homological torsion

The strategy behind our proof diverges quite a bit from the 3-manifold case. There, geometry does much of the work. Here, we lean more on combinatorics: the structure of graphs, and more importantly, how local data at vertex groups shapes the global behavior of the whole group.

Instead of attaching roots to surfaces with boundary, we use a different model for producing homological torsion: *branched surfaces*. These are collections of compact, orientable surfaces with boundary, glued together along their boundary components. Each surface in a branched surface $B$ defines a relation in abelianization—for example, a surface with boundary components $\sigma_1, \ldots, \sigma_k$ contributes an equation of the form 

$$ [\sigma] \pm [\sigma_2] \pm \cdots \pm [\sigma_k] = 0 $$  

in the abelianization of $B$. We refer to these as $\partial$-*equations*. Branched surfaces thus provide a geometric realization of systems of such linear relations.

The first step in our argument is to show that every system of linear equations in a free abelian group is equivalent (in the sense of yielding the same quotient) to one arising from a branched surface. In particular, a simple type of branched surface—three orientable surfaces of positive genus, each with a single boundary component and glued along those boundaries—admits finite covers whose first homology contains arbitrary torsion. We call this a *triple branched surface*.

Note that branched surfaces are themselves graphs of free groups with cyclic edge groups; the fact that any branched surface has a *precover* that is a triple branched surface proves the theorem in this case.

>**Example.** Suppose $B$ is a triple branched surface made up of three surfaces $\Sigma$, $\Theta$, and $\Pi$, each with a single boundary circle identified as a common curve $x$. The table below describes a 4-sheeted cover $B' \to B$ in which $\Sigma$, $\Theta$, and $\Pi$ each lift to two> copies, and the common boundary $x$ lifts to four distinct loops $x_1, x_2, x_3, x_4$. A check mark indicates that the boundary of the given surface copy maps to the corresponding lift of $x$. This cover has $H_1(B') \cong \mathbb{Z}^n \oplus \mathbb{Z}/2\mathbb{Z}$.

<div align="center">
  <table>
    <thead>
      <tr>
        <th></th>
        <th>$\Sigma_1$</th>
        <th>$\Sigma_2$</th>
        <th>$\Theta_1$</th>
        <th>$\Theta_2$</th>
        <th>$\Pi_1$</th>
        <th>$\Pi_2$</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>$x_1$</td>
        <td>✔</td>
        <td></td>
        <td>✔</td>
        <td></td>
        <td>✔</td>
        <td></td>
      </tr>
      <tr>
        <td>$x_2$</td>
        <td>✔</td>
        <td></td>
        <td></td>
        <td>✔</td>
        <td></td>
        <td>✔</td>
      </tr>
      <tr>
        <td>$x_3$</td>
        <td></td>
        <td>✔</td>
        <td></td>
        <td>✔</td>
        <td>✔</td>
        <td></td>
      </tr>
      <tr>
        <td>$x_4$</td>
        <td></td>
        <td>✔</td>
        <td>✔</td>
        <td></td>
        <td></td>
        <td>✔</td>
      </tr>
    </tbody>
  </table>
</div>

>Indeed, in $H_1(B')$, we have that $x_i+x_j=0$ for every $i<j\le 4$, which simplifies to $x_1=x_2=x_3=x_4$ and $2\cdot x_1 = 0$.
<div align="center">
  <img src="example.png" style="max-width: 100%; width: 700px;" />
</div>

---
### The general case

Having established the result for branched surfaces—and given that hyperbolic graphs of free groups with cyclic edge groups admit local retractions—it now suffices to find a branched surface inside such a group $G$ (as we will see, it is unclear whether this is always possible). This reduces the general case to a geometric problem: constructing a branched surface within $G$. Wilton proved that, unless $G$ is free, it must contain a surface subgroup. More precisely:

>Theorem (Wilton '18): Let $F$ be a free group which is freely indecomposable relative to $w_1,\ldots,w_n \in F$. Then there is a surface with boundary $\Sigma$ and an embedding $f:\pi_1(\Sigma)\hookrightarrow F$ such that
>- the image of every component of $\partial(\Sigma)$ is an elevation of some $w_i$ to $f(\pi_1(\Sigma))\le F$. and
>- the total degree of the elevations of $w_i$ to $f(\pi_1(\Sigma))$ is uniform across all $i\le n$.
 
In Wilton's proof, the non-freeness of $G$ serves as a lower bound on the complexity of vertex links in a graph of spaces decomposition of $G$. Specifically, if $G$ is not free, then it contains a one-ended graph of free groups with cyclic edge groups, say $G'$, in which—by an old result of Shanitzer—every vertex group is freely indecomposable relative to the incident edge groups. Wilton’s theorem applies to each such vertex, and the resulting surfaces can be glued together to produce a global surface subgroup inside $G$.

In our setting, the hypothesis that $G$ is not a free product of free and surface groups (in which case, the abelianization of every finite-index subgroup of $G$ is always a free abelian group) yields a sharper complexity threshold, which can manifest in one of two ways:

1. **"Triple intersections".** Three distinct cyclic subgroups of $G$ are identified—this creates branching behaviour in the underlying graph, and we can again insert surfaces à la Wilton at each vertex to build a branched surface.

2. **Rigid vertices**. The cyclic JSJ decomposition of $G$ contains a rigid piece.

The second case is a lot more subtle, and most of our efforts are directed toward resolving it.

---
### Artificial branching

so we proved the case of branched surfaces - and as a result, since hyperbolic graphs of free groups with cyclic edges admit local retractions, to prove the result in the general case, it is enough to find a branched surface inside such $G$. Wilton showed that unless $G$ is free, then it must contain a surface subgroup. More precisely, he proved the following theorem:
>**Theorem [Wilton '18]:** fill in later

The surfaces produced by Wilton's theorem can be combined to form a surface inside $G$. In his proof, Wilton used the fact that $G$ is not free as a lower complexity bound on links of vertices in a graph of spaces decomposition of $G$. More specifically, if $G$ is not free, then it contains a one-ended graph of free groups with cyclic edges $G'$, in which by an old theorem of Shanitzer every vertex group is freely decomposable relative to the adjacent edge groups. Wilton's theorem above can be applied to each vertex, and the resulting surfaces can be combined to build a surface subgroup of $G$. In our case, the assumption that $G$ is not a free product of free and surface groups, gives a sharper lower bound on the complexity of $G$. This complexity bound can appear in one of two forms:
1. three different cyclic subgroups of $G$ are identified. In this case the underlying graph of $G$ exhibits a "branching behaviour", and one can replace each vertex group with a surface as in Wilton's theorem to construct a branched surface inside $G$.
2. The cyclic JSJ decomposition of $G$ contains a rigid vertex.

Case 2. above is much harder to deal with, and the bulk of our proof is devoted to this case.

---


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
