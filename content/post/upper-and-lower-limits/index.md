---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Upper and Lower Limits"
subtitle: "blah lah"
summary: "kop pop"
authors: []
tags: []
categories: []
date: 2020-06-19T16:33:53-04:00
lastmod: 2020-06-19T16:33:53-04:00
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

## Preliminaries
In the spirit of keeping this article fairly independent and establishing a common notation, let's review some preliminaries.

**Definition:** Suppose $S$ is an ordered set, and $E \subset S$. If there exists a $\beta \in S$ such that $x \leq \beta$ for every $x \in E$, we say that $E$ is *bounded above*, and call $\beta$ an *upper bound* of $E$.

Lower bounds are defined in the same way with $\geq$ in place of $\leq$.

**Definition:** Suppose $S$ is an ordered set, $E \subset S$, and $E$ is bounded above. Suppose there exists an $\alpha \in S$ with the following properties:

1. $\alpha$ is an upper bound of $E$.
2. If $\gamma < \alpha$ then $\gamma$ is not an upper bound of $E$.

Then $\alpha$ is called the *least upper bound* of $E$ or the *supremum* of $E$, and we write
$$
\alpha = \sup E
$$
That there is at most one supremum is clear from the property 2 above. The *greatest lower bound*, or *infimum*, of a set $E$ which is bounded below is defined in the same manner, and we write it as $\inf E$. Note that if $x \in E$, $\alpha = \sup E$, and $x < \alpha$ then there exists $y \in E$ such that $x < y < \alpha$ because otherwise $x$ would a lower bound less than $\alpha$.
