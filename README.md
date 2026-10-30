# econ3916-lab10-causal-logic

# Correlation & Causality: Confounders, Colliders and the Limits of Controls

## Objective
In this lab, I explored why correlation does not always mean causation and how controlling for different variables can affect regression results.

## Methodology
- Simulated three situations: causation, confounding, and selection bias.
- Used NetworkX to draw DAGs for confounders, colliders, and mediators.
- Compared regression results with and without control variables.
- Created an M-bias example and wrote `coef_on_d()` to test different controls.
- Compared experimental and observational estimates using the LaLonde dataset.
- Examined how sample size affects confidence intervals and bias.

## Key Findings
- The three simulations showed similar correlations of around 0.65, even though their true causal effects were different.
- Controlling for a confounder improved the estimate, but controlling for a collider created a false relationship.
- In the collider example, the estimated coefficient was -0.592, even though the true effect was 0.
- In the M-bias example, controlling for W gave an estimate of -0.191. Adding u1 changed it to 0.006, which was close to the true effect of 0.
- In the LaLonde analysis, the experimental estimate was $1,794, while the naive observational estimate was -$8,498. After adding controls, the estimate became $699, closing 89% of the gap.
- Increasing the sample size made confidence intervals narrower but did not remove bias.

## Conclusion
I learned that adding more controls does not always improve a regression. It is important to understand the relationships between variables before deciding what to control for.
