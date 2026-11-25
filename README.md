# Sharp $\Omega\!\left(\kappa^{1/p_{\mathrm{sil}}}\log(1/\varepsilon)\right)$ Lower Bound for Gradient Descent on Strongly Convex Objectives

**Yuhan Ye · November 25, 2026 · v0.4**

[Abstract and publication history](https://yeyuhanyyh.github.io/strongly-convex-silver-lower-bound/) · [Read the PDF](https://yeyuhanyyh.github.io/strongly-convex-silver-lower-bound/manuscript.pdf) · [LaTeX source](manuscript.tex)

For smooth strongly convex objectives with condition number $\kappa$, consider gradient descent with any predetermined sequence of real stepsizes. To reduce either the squared distance to the minimizer or function suboptimality by a factor $\varepsilon$, the worst-case number of iterations is at least

$$
\Omega\!\left(\kappa^{1/p_{\mathrm{sil}}}\log(1/\varepsilon)\right),
\qquad p_{\mathrm{sil}}=\log_2(1+\sqrt{2}).
$$

The lower bound holds for sufficiently large $\kappa$ and every $0<\varepsilon<1$. For $0<\varepsilon\le1/2$, it matches the silver upper bound up to an absolute constant. Each error is measured relative to its initial value and has its own worst case.

## Proof

Section 2 constructs a hard function when the sum of the positive stepsizes, each capped at a fixed threshold, is small enough. Section 3 shows that any schedule that guarantees a reduction must satisfy this bound. The appendix gives the estimates behind the two arguments and shows how the prescribed GD trajectories can occur on a single strongly convex objective. The proof adapts the checkpoint construction of Liu and Ye and the threshold count of Jeong and Hong. [Liu and Ye](https://arxiv.org/abs/2609.26873v2) · [Jeong and Hong](https://arxiv.org/abs/2611.30100v1)

OpenAI Codex assisted in developing the proof and writing the manuscript. Comments on the proof are welcome through [GitHub Issues](https://github.com/yeyuhanyyh/strongly-convex-silver-lower-bound/issues).

## Versions and source

The [first version](https://github.com/yeyuhanyyh/strongly-convex-silver-lower-bound/tree/v0.1), posted November 24, 2026, treats nonnegative stepsizes. The [real-stepsize result](https://github.com/yeyuhanyyh/strongly-convex-silver-lower-bound/tree/v0.2) was posted November 25. Version 0.3 reorganized the proofs. Version 0.4 explains the smooth convex argument of Jeong and Hong and revises the proofs of Lemmas 2 and 3.

Compile the self-contained source by running `pdflatex manuscript.tex` twice. Citation metadata are available in [CITATION.cff](CITATION.cff).
