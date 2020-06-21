---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Partitions and Equivalence Relations"
subtitle: ""
summary: "I want to show how these two concepts are a single mathematical idea."
authors: []
tags: []
categories: []
date: 2020-06-20T19:16:45-04:00
lastmod: 2020-06-20T19:16:45-04:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

I want to show how these two concepts are a single mathematical idea.

## Partition
The concept of partition is integral in understanding equivalence relations.

A *partition* of a non-empty set, $X$, is a disjoint class $\\{X_i\\}_{i \in I}$ of non-empty subsets of $X$ whose union is $X$. The $X_i$'s are called the *partition sets*.

For example, if $X = \mathbb{R}$, then $X$ can be partitioned as
$$
X = \bigcup_{n \in \mathbb{Z}}[n, n+1)
$$

## Binary Relation
A *binary relation*, or simply *relation*, $R$, in the set $X$ is a subset of $X \times X$.

For $x, y \in X$, we denote the fact $(x,y) \in R$ by writing $x R y$. A function may be defined as a special kind of binary relation.

## Equivalence relation
Let's assume that a partition of our non-empty set $X$ is given, and we associate with this partition a relation, $\sim$, in $X$ defined as follows: $x \sim y$ if $x$ and $y$ belong to the same partition set. It can easily checked that the relation $\sim$ satisfies:
1. $x \sim x$ for every $x \in X$ (*reflexivity*);
2. $x \sim y \implies y \sim x$ (*symmetry*);
3. $x \sim y$ and $y \sim z$ $\implies$ $x \sim z$ (*transitivity*).

Any relation in $X$ which possesses these three properties is called an *equivalence relation* in $X$.

### Examples
1. Let $X = \mathbb{Z}$ and let $x \sim y$ if $2 | x-y$ for $x,y \in X$. Then clearly $\sim$ is an equivalence relation in $X$.
2. Let $X$, $Y$ be any non-empty sets and $f$ be a mapping from $X$ onto $Y$. Let $x \sim y$ if $f(x) = f(y)$ for $x,y \in A$. This defines an equivalence relation in $X$. Indeed, $f(x) = f(x)$, and so $x \sim x$. If $f(x) = f(y)$ then $f(y) = f(x)$, and so $x \sim y \implies y \sim x$. Finally, if $f(x) = f(y)$ and $f(y) = f(z)$ then $f(x) = f(z)$, and so $x \sim y$ and $y \sim z$ $\implies$ $x \sim z$. The first example is a special case of this one if we take $X = \mathbb{Z}$, $Y = \\{0,1\\}$ and $f(x) = x \mod 2$.

### "Relation" to partition
We have just seen that each partition of $X$ has associated with it a natural equivalence relation in $X$. Let us now reverse the situation and show that a given equivalence relation in $X$ determines a natural partition of $X$.

Let $\sim$ be an equivalence relation in $X$. For every $x \in X$ define the set
$$
[x] := \\{ y \in X : y \sim x\\}
$$
called the *equivalence set* of $x$. We show that the class of all distinct equivalence sets forms a partition of $X$.

By reflexivity, $x \in [x]$ for every $x \in X$, and thus each equivalence set is non-empty and their union is $X$. We now need to show that any two equivalence sets $[x_1]$ and $[x_2]$ are either disjoint or identical. We prove this by showing that if $[x_1]$ and $[x_2]$ are not disjoint then they are identical. To this end, let $z$ be a common element of $[x_1]$ and $[x_2]$. Let $y$ be any element of $[x_1]$. Using transitivity,
$$
y \sim x_1 \sim z \sim x_2
$$
Therefore, $y \in [x_2]$. Since $y$ was an arbitrary element of $[x_1]$, we get $[x_1] \subseteq [x_2]$. We can similarly show that $[x_2] \subseteq [x_1]$. In short, $[x_1] = [x_2]$.

We have shown that there is no real distinction between partitions of a set and equivalence relations in the set. They are two "equivalent" approaches for the same mathematical idea. The approach we choose in an application depends entirely on our own convenience.