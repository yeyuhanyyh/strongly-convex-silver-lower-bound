# Sharp $\Omega\!\left(\kappa^{1/p_{\mathrm{sil}}}\log(1/\varepsilon)\right)$ Lower Bound for Gradient Descent on Strongly Convex Objectives

**Yuhan Ye · November 25, 2026 · v0.2**

[Read the manuscript (PDF)](manuscript.pdf) · [LaTeX source](manuscript.tex)

For smooth strongly convex objectives with condition number $\kappa$, consider gradient descent with any predetermined sequence of real stepsizes. To reduce either the squared distance to the minimizer or function suboptimality by a factor $\varepsilon$, the worst-case number of iterations is at least

$$
\Omega\!\left(\kappa^{1/p_{\mathrm{sil}}}\log(1/\varepsilon)\right),
\qquad p_{\mathrm{sil}}=\log_2(1+\sqrt{2}).
$$

The lower bound holds for sufficiently large $\kappa$ and every $0<\varepsilon<1$. For $0<\varepsilon\le1/2$, it matches the silver upper bound up to an absolute constant. Each error is measured relative to its initial value and has its own worst case.

Section 2 adapts Liu and Ye's checkpoint construction to schedules containing negative steps. Section 3 adapts Jeong and Hong's method of counting steps above a varying threshold. The appendix shows how to join the resulting trajectories on one strongly convex function. One step uses smooth convex interpolation to change part of the objective near a checkpoint while preserving prescribed values and gradients farther away. [Liu and Ye](https://arxiv.org/abs/2609.26873v2) · [Jeong and Hong](https://arxiv.org/abs/2611.30100v1) · [Taylor, Hendrickx, and Glineur](https://doi.org/10.1007/s10107-016-1009-3)

OpenAI Codex assisted in developing the proof and writing the manuscript. Comments on the proof are welcome through [GitHub Issues](https://github.com/yeyuhanyyh/strongly-convex-silver-lower-bound/issues).

Compile the self-contained source by running `pdflatex manuscript.tex` twice. The [earlier version](https://github.com/yeyuhanyyh/strongly-convex-silver-lower-bound/tree/v0.1) treats nonnegative stepsizes.
