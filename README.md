# A sharp silver lower bound for gradient descent on strongly convex functions

**Yuhan Ye · Research manuscript · v0.1 · November 24, 2026**

[Read the PDF](manuscript.pdf) · [View the self-contained LaTeX source](manuscript.tex)

## The bound

Let $p=\log_2(1+\sqrt{2})$. Consider gradient descent with a predetermined schedule of nonnegative stepsizes on smooth strongly convex functions of condition number $\kappa$. For all sufficiently large $\kappa$, the manuscript gives the iteration lower bound

$$
\Omega\!\left(\kappa^{1/p}\log(1/\varepsilon)\right).
$$

This holds for every $0<\varepsilon<1$, for reducing either squared distance to the minimizer or function suboptimality relative to its initial value. Each criterion takes its own worst case over finite dimensions. The constant is independent of the schedule, the horizon, the condition number, and the accuracy.

## Guide to the proof

- **Section 1** reduces the theorem to two statements about the same sum of truncated stepsizes.
- **Section 2** uses a bound on this sum to partition the schedule and construct a strongly convex objective on which GD makes slow progress.
- **Section 3** bounds the truncated sum by counting steps above each threshold. **Sections 4 and 5** realize the trajectories needed for that count on a single strongly convex objective.

The silver schedule is due to Altschuler and Parrilo. Liu and Ye established the strongly convex lower bound with exponent $1/p-o(1)$ and developed the local bending and repair constructions used here. Jeong and Hong proved the sharp rate in the smooth convex setting and developed the multiscale counting and trajectory arguments adapted here. The manuscript identifies the specific results used from each paper. [Altschuler and Parrilo](https://doi.org/10.1145/3708502) · [Liu and Ye, v2](https://arxiv.org/abs/2609.26873v2) · [Jeong and Hong, v1](https://arxiv.org/abs/2611.30100v1)

## Status and reproduction

This is a public research draft for independent verification. OpenAI Codex contributed to the proof development, checks of intermediate estimates, and writing. Corrections that identify a specific section or inequality are welcome through [GitHub Issues](https://github.com/yeyuhanyyh/strongly-convex-silver-lower-bound/issues).

To build the PDF with a standard LaTeX installation, run `pdflatex manuscript.tex` twice. The bibliography is included in the source. To cite a particular revision, include the version tag or commit hash.
