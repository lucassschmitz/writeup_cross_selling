# Equilibrium Characterization with Switching Costs

## Overview

This document derives the equilibrium mixed strategies for the extended model with switching cost $\lambda$. We have established through Steps 1-13 that:

- **Outside bank support:** $[\ell_o, u_o] = [r_p, r_F]$
- **Inside bank support for S-firms:** $[\ell_i^S, u_i^S] = [r_p + \lambda, r_F + \lambda]$
- **Inside bank strategy for F-firms:** Point mass at $r_F + \lambda$
- **Outside bank expected profits:** Zero
- **Both $H_i^S$ and $H_o$ are continuous and strictly increasing** on their respective supports (except $H_o$ may have an atom at $r_F$)

---

## Deriving the Equilibrium Distributions

### The Indifference Conditions

For a mixed strategy equilibrium, each player must be indifferent over all rates in their support.

**Inside bank's profit function (for S-firms):**

From Eq. (A.5), when the inside bank offers rate $r_i$ to an S-firm:

$$P_i^S(r_i) = \bigl(1 - H_o((r_i - \lambda)^-)\bigr)\bigl[p(S)(1+r_i) - (1+\bar{r})\bigr]$$

The inside bank wins if the outside bank's offer $r_o$ satisfies $r_o > r_i - \lambda$ (i.e., the firm prefers staying with the inside bank at $r_i$ over switching and paying $r_o + \lambda$).

**Outside bank's profit function:**

From Eq. (A.6), when the outside bank offers rate $r_o$:

$$P_o(r_o) = p\bigl(1 - H_i^S(r_o + \lambda)\bigr)\bigl[p(S)(1+r_o) - (1+\bar{r})\bigr] + (1-p)\bigl(1 - H_i^F(r_o + \lambda)\bigr)\bigl[p(F)(1+r_o) - (1+\bar{r})\bigr]$$

Since $H_i^F$ is a point mass at $r_F + \lambda$, we have:
- For $r_o < r_F$: $H_i^F(r_o + \lambda) = 0$
- For $r_o \geq r_F$: $H_i^F(r_o + \lambda) = 1$

---

### Simplification for $r_o \in [r_p, r_F)$

For $r_o \in [r_p, r_F)$, the outside bank's profit becomes:

$$P_o(r_o) = p\bigl(1 - H_i^S(r_o + \lambda)\bigr)\bigl[p(S)(1+r_o) - (1+\bar{r})\bigr] + (1-p)\bigl[p(F)(1+r_o) - (1+\bar{r})\bigr]$$

---

### Setting Up the Equilibrium Equations

**Step A: Outside bank makes zero profit (from Step 10)**

Setting $P_o(r_o) = 0$ for all $r_o \in [r_p, r_F)$:

$$p\bigl(1 - H_i^S(r_o + \lambda)\bigr)\bigl[p(S)(1+r_o) - (1+\bar{r})\bigr] + (1-p)\bigl[p(F)(1+r_o) - (1+\bar{r})\bigr] = 0$$

**Step B: Inside bank's profit is constant**

For the inside bank offering $r_i \in [r_p + \lambda, r_F + \lambda]$, let $r = r_i - \lambda$ (so $r \in [r_p, r_F]$):

$$P_i^S(r + \lambda) = \bigl(1 - H_o(r^-)\bigr)\bigl[p(S)(1+r+\lambda) - (1+\bar{r})\bigr] = c$$

for some constant $c > 0$.

---

### Solving for $H_i^S$

From the zero-profit condition for the outside bank:

$$p\bigl(1 - H_i^S(r + \lambda)\bigr)\bigl[p(S)(1+r) - (1+\bar{r})\bigr] = -(1-p)\bigl[p(F)(1+r) - (1+\bar{r})\bigr]$$

Note that $p(F)(1+r) - (1+\bar{r}) < 0$ for $r < r_F$, so the RHS is positive.

Let me define for convenience:
- $\pi_S(r) = p(S)(1+r) - (1+\bar{r})$ (profit margin on S-firm at rate $r$)
- $\pi_F(r) = p(F)(1+r) - (1+\bar{r})$ (profit margin on F-firm at rate $r$)

Then:

$$1 - H_i^S(r + \lambda) = -\frac{(1-p)\pi_F(r)}{p \cdot \pi_S(r)}$$

Since $\pi_F(r) < 0$ for $r < r_F$:

$$H_i^S(r + \lambda) = 1 + \frac{(1-p)\pi_F(r)}{p \cdot \pi_S(r)} = \frac{p \cdot \pi_S(r) + (1-p)\pi_F(r)}{p \cdot \pi_S(r)}$$

The numerator is:

$$p[p(S)(1+r) - (1+\bar{r})] + (1-p)[p(F)(1+r) - (1+\bar{r})]$$

$$= [p \cdot p(S) + (1-p)p(F)](1+r) - (1+\bar{r})$$

$$= p_{pool}(1+r) - (1+\bar{r})$$

where $p_{pool} = p \cdot p(S) + (1-p)p(F)$ is the pooling probability. By definition of $r_p$: $p_{pool}(1+r_p) = (1+\bar{r})$.

Therefore:

$$H_i^S(r + \lambda) = \frac{p_{pool}(1+r) - (1+\bar{r})}{p[p(S)(1+r) - (1+\bar{r})]}$$

Simplifying using $1+\bar{r} = p_{pool}(1+r_p)$:

$$H_i^S(r + \lambda) = \frac{p_{pool}(r - r_p)}{p \cdot \pi_S(r)}$$

---

### Solving for $H_o$

From the inside bank's indifference condition:

$$\bigl(1 - H_o(r)\bigr)\bigl[p(S)(1+r+\lambda) - (1+\bar{r})\bigr] = c$$

At $r = r_p$ (where $H_o(r_p) = 0$):

$$c = p(S)(1+r_p+\lambda) - (1+\bar{r}) = p(S)(r_p + \lambda - r_S)$$

where we used $1+\bar{r} = p(S)(1+r_S)$.

Therefore:

$$1 - H_o(r) = \frac{p(S)(r_p + \lambda - r_S)}{p(S)(1+r+\lambda) - (1+\bar{r})} = \frac{p(S)(r_p - r_S) + p(S)\lambda}{p(S)(r - r_S) + p(S)\lambda}$$

$$H_o(r) = 1 - \frac{r_p - r_S + \lambda}{r - r_S + \lambda} = \frac{r - r_p}{r - r_S + \lambda}$$

---

### Verification of Boundary Conditions

**For $H_i^S$:**
- At $r = r_p$: $H_i^S(r_p + \lambda) = 0$ ✓
- At $r = r_F$: Need to verify $H_i^S(r_F + \lambda) = 1$

Using the identity $(r_F - r_p) = \frac{p \cdot \pi_S(r_F)}{p_{pool}}$ (which follows from the Sharpe model structure):

$$H_i^S(r_F + \lambda) = \frac{p_{pool}(r_F - r_p)}{p \cdot \pi_S(r_F)} = 1$$ ✓

**For $H_o$:**
- At $r = r_p$: $H_o(r_p) = 0$ ✓
- At $r = r_F$: 

$$H_o(r_F^-) = \frac{r_F - r_p}{r_F - r_S + \lambda}$$

Since $r_F - r_S > r_F - r_p$ (as $r_S < r_p$), and $\lambda > 0$, we have $H_o(r_F^-) < 1$.

Therefore, **$H_o$ has an atom at $r_F$** with mass:

$$1 - H_o(r_F^-) = 1 - \frac{r_F - r_p}{r_F - r_S + \lambda} = \frac{r_F - r_S + \lambda - (r_F - r_p)}{r_F - r_S + \lambda} = \frac{r_p - r_S + \lambda}{r_F - r_S + \lambda}$$

---

## Summary: Equilibrium Mixed Strategies

### Inside Bank

**For S-firms:** Atomless distribution on $[r_p + \lambda, r_F + \lambda]$ with CDF:

$$\boxed{H_i^S(r + \lambda) = \frac{p_{pool}(r - r_p)}{p[p(S)(1+r) - (1+\bar{r})]}, \quad r \in [r_p, r_F]}$$

**For F-firms:** Point mass at $r_F + \lambda$

### Outside Bank

Distribution on $[r_p, r_F]$ with:

- Atomless part on $[r_p, r_F)$ with CDF:

$$\boxed{H_o(r) = \frac{r - r_p}{r - r_S + \lambda}, \quad r \in [r_p, r_F)}$$

- Point mass at $r_F$ of size:

$$\boxed{\Delta H_o(r_F) = \frac{r_p - r_S + \lambda}{r_F - r_S + \lambda}}$$

---

## Key Differences from Original Model ($\lambda = 0$)

1. **Inside bank's support shifts up by $\lambda$**: The inside bank exploits the switching cost by offering higher rates.

2. **Outside bank's distribution changes**: The atom at $r_F$ is now $\frac{r_p - r_S + \lambda}{r_F - r_S + \lambda}$ instead of the original expression.

3. **Inside bank's expected profits increase**: The constant profit level is $c = p(S)(r_p - r_S + \lambda)$ compared to $p(S)(r_p - r_S)$ in the original model.

---

## Equilibrium Expected Profits

**Inside bank:**
- On S-firms: $\Pi_i^S = p \cdot c = p \cdot p(S)(r_p - r_S + \lambda)$
- On F-firms: Zero (offers break-even rate $r_F + \lambda$, but F-firms switch to outside bank when outside offers below $r_F$)

**Outside bank:** Zero expected profit (by Step 10)

---

## Switching Probability

A firm switches when $r_o + \lambda < r_i$, i.e., when $r_o < r_i - \lambda$.

**S-firms switch with probability:**

$$\Pr(\text{S switches}) = \int_{r_p}^{r_F} H_o(r) \cdot h_i^S(r+\lambda) \, dr$$

**F-firms switch with probability:**

$$\Pr(\text{F switches}) = H_o(r_F^-) = \frac{r_F - r_p}{r_F - r_S + \lambda}$$

The switching probability decreases with $\lambda$, reflecting the lock-in effect of switching costs.

---

## Open Questions / Items to Verify

1. **Verification of $H_i^S(r_F + \lambda) = 1$**: The identity used needs to be confirmed from the original model structure.

2. **Behavior at the atom**: Need to confirm the tie-breaking rule at $r_F$ is consistent with equilibrium.

3. **Existence condition**: What parameter restrictions ensure this equilibrium exists (e.g., $\lambda$ not too large)?

---

## Comments Section

<!-- Leave your comments below this line -->


