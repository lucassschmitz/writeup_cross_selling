# Model Files

## Core Models

**Model 1** (M1_switching costs.tex, v1, v2): Multi-product firms with switching costs. Two-period duopoly where consumers choose a firm for product 1 (e.g., checking account) and later for product 2 (e.g., loan). Incur switching cost $s$ if changing firms between periods. Consumer utility includes persistent heterogeneity $\mu_{ij}$.
- M1_identification.tex: Estimation strategy using BLP with demand parameters identified from first-period choices.

**Model 2** (M2_extension Sharpe.tex): Sharpe (1990) extended with switching costs à la von Thadden (2004). Firms seek sequential project financing. Inside banks observe project outcomes; outside banks don't. Switching between banks costs $\lambda$.

**Model 3** (M3_extension Allen et al..tex): Consumer mortgage choice with search costs. Consumers choose among lenders, with home bank offering differentiated value $\lambda$. Search cost $k$ to obtain quotes from additional lenders. Home bank has cost advantage $\Delta$ for cross-selling.

**Model 4** (M4_adapting Engelbrecht et al.tex): Adapts Engelbrecht-Wiggans et al. (1983) auction framework with switching costs. Informed incumbent (bank 1) observes borrower default probability $h$; uninformed entrant (bank 2) does not. Incumbent plays pure strategy $\sigma(h) = \lambda + \mu(h)^{-1}$; entrant plays mixed strategy $G(x)$. Type distribution $F(h)$ is generic.
- M4_identification.tex: Identification strategy using Kumaraswamy distribution; parameters ($\lambda$, $\alpha$, $\beta$) identified from winning rates, winner identity, and default outcomes.

**Model 5** (M5_convert4intostructural.tex): Full structural model of cross-selling. Two-stage game: stage 1 (introductory product) generates information asymmetry and switching costs; stage 2 (loan market) solved via backward induction. Logit demand with price sensitivity $\alpha$ and switching cost $\lambda$. Bank 1 plays type-contingent strategy $\sigma^*(h)$; bank 2 sets single rate $r_2^*$.
- M5_identification.tex: Nonparametric and parametric identification. Establishes that entrant rate $r_2$ is a sufficient statistic for unobserved public covariates $\mathbf{x}$, enabling estimation without observing borrower characteristics.

**Model 6** (M6_heterogeneity_information.tex, v2): Extends Model 5 with observable heterogeneity. Both banks observe public covariates $\mathbf{x}$; incumbent additionally observes private covariates $\mathbf{x}'$. Equilibrium is conditional on $\mathbf{x}$: bank 2 sets $r_2^*(\mathbf{x})$, bank 1 plays $\sigma^*(h; \mathbf{x})$. Identification and likelihood developed for estimation.

**Model 7** (M7_heterogeneity.tex): Structural heterogeneity without borrower observables. Generates variation in entrant rates through (1) loan-level cost-of-funds shifters $Z$ (maturity, collateral, market conditions) and (2) supply-side pricing shocks, rather than requiring observable borrower characteristics. Cost of funds: $c_{0i} = \bar{c}_0 + Z_i'\delta$. Maintains M5 core structure while enabling estimation when borrower covariates are unavailable.

## Reference Models

**von_thadden_original.tex**: Original von Thadden (2004) framework
**allen et al. (2019 JPE) model.tex**: Allen et al. reference model
**hendricks and porter model.tex**: Hendricks and Porter reference model
 