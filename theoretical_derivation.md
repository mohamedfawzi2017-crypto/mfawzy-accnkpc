# Micro-Foundations and Mathematical Derivation of the Asymmetric Cost-Channel New Keynesian Phillips Curve (ACC-NKPC)

**Author:** Mohamed Fawzy AbdulAziz  
**Affiliation:** Cairo University & Information and Decision Support Center (IDSC), Egyptian Cabinet  
**Target Journal:** *The Journal of Economic Asymmetries* (Elsevier - CiteScore 7.4, Q1)

---

## 1. Model Environment & Micro-Foundations

We consider a small open emerging economy populated by a continuum of monopolistically competitive domestic intermediate firms indexed by $j \in [0, 1]$, a representative household, and a central bank implementing monetary policy.

### 1.1 Representative Household Preferences
The representative household maximizes expected discounted lifetime utility:
$$\max_{\{C_t, L_t, B_t\}} \mathbb{E}_0 \sum_{t=0}^{\infty} \beta^t \left[ \frac{C_t^{1-\sigma}}{1-\sigma} - \frac{L_t^{1+\varphi}}{1+\varphi} \right]$$
where $\beta \in (0, 1)$ is the subjective discount factor, $\sigma > 0$ is the coefficient of relative risk aversion (inverse intertemporal elasticity of substitution), $\varphi > 0$ is the inverse Frisch elasticity of labor supply, $C_t$ is aggregate composite consumption, and $L_t$ is total labor hours supplied.

The flow budget constraint is given by:
$$P_t C_t + \frac{B_t}{1 + i_t} \le B_{t-1} + W_t L_t + \Pi_t + T_t$$
where $P_t$ is the domestic consumer price index (CPI), $B_t$ denotes nominal bond holdings paying a gross nominal interest rate $1 + i_t$, $W_t$ is the nominal wage, $\Pi_t = \int_0^1 \Pi_t(j) dj$ represents aggregate firm dividends, and $T_t$ denotes lump-sum government transfers/taxes.

The first-order conditions yield the standard consumption Euler equation and labor supply relation:
$$\beta (1 + i_t) \mathbb{E}_t \left[ \left( \frac{C_{t+1}}{C_t} \right)^{-\sigma} \frac{P_t}{P_{t+1}} \right] = 1$$
$$\frac{W_t}{P_t} = C_t^\sigma L_t^\varphi$$

Log-linearizing around the steady state yields the Dynamic IS curve:
$$\tilde{y}_t = \mathbb{E}_t[\tilde{y}_{t+1}] - \frac{1}{\sigma} (i_t - \mathbb{E}_t[\pi_{t+1}] - r_t^n)$$
where $\tilde{y}_t = y_t - y_t^n$ is the output gap, $\pi_{t+1} = \ln P_{t+1} - \ln P_t$, and $r_t^n$ is the natural real rate of interest.

---

## 2. Production Technology with Working Capital Credit Constraint

Each intermediate firm $j \in [0, 1]$ produces a differentiated good $Y_t(j)$ using a Cobb-Douglas production technology combining domestic labor $L_t(j)$ and imported intermediate inputs $M_t(j)$:
$$Y_t(j) = A_t L_t(j)^{1-\alpha} M_t(j)^\alpha, \quad \alpha \in (0, 1)$$
where $A_t$ is total factor productivity, and $\alpha$ is the share of imported inputs in gross domestic output.

### 2.1 The Working Capital Channel (Cost Channel)
Following Barth & Ramey (2001) and Ravenna & Walsh (2006), firms face a cash-in-advance constraint on their working capital: they must borrow from commercial banks at the gross lending rate $(1 + i_t^L)$ to pay for a fraction $\phi_L \in [0, 1]$ of the wage bill and a fraction $\phi_M \in [0, 1]$ of imported input costs prior to revenue realization.

Let $i_t^L$ be linked to the central bank policy rate $i_t$ via commercial bank lending markup:
$$i_t^L = i_t + \mu_t^b$$
where $\mu_t^b$ is the banking spread.

The total nominal cost of firm $j$ is given by:
$$TC_t(j) = W_t L_t(j) \cdot (1 + \phi_L i_t^L) + E_t P_t^* M_t(j) \cdot (1 + \phi_M i_t^L)$$
where $E_t$ is the nominal exchange rate (local currency units per foreign currency unit, EGP/USD) and $P_t^*$ is the foreign price index of intermediate goods.

### 2.2 Cost Minimization and Nominal Marginal Cost
Minimizing $TC_t(j)$ subject to the production constraint yields the input optimality condition:
$$\frac{W_t (1 + \phi_L i_t^L)}{E_t P_t^* (1 + \phi_M i_t^L)} = \frac{1-\alpha}{\alpha} \frac{M_t(j)}{L_t(j)}$$

Solving for nominal marginal cost $MC_t(j)$:
$$MC_t(j) = \frac{1}{A_t} \left( \frac{W_t (1 + \phi_L i_t^L)}{1-\alpha} \right)^{1-\alpha} \left( \frac{E_t P_t^* (1 + \phi_M i_t^L)}{\alpha} \right)^\alpha$$

Assuming symmetric working capital intensity $\phi_L = \phi_M = \phi$:
$$MC_t = \frac{1}{A_t} \left( \frac{W_t}{1-\alpha} \right)^{1-\alpha} \left( \frac{E_t P_t^*}{\alpha} \right)^\alpha (1 + \phi i_t^L)$$

Real marginal cost $mc_t = \frac{MC_t}{P_t}$ is therefore:
$$mc_t = \frac{1}{A_t} \left( \frac{W_t/P_t}{1-\alpha} \right)^{1-\alpha} \left( \frac{E_t P_t^* / P_t}{\alpha} \right)^\alpha (1 + \phi i_t^L)$$

Log-linearizing $mc_t$ around the zero-inflation steady state ($\hat{mc}_t = \ln mc_t - \ln mc_{ss}$):
$$\hat{mc}_t = (1-\alpha) \hat{w}_t^r + \alpha \hat{q}_t + \phi \cdot \tilde{i}_t - \hat{a}_t$$
where:
* $\hat{w}_t^r = \hat{w}_t - \hat{p}_t = \sigma \tilde{y}_t + \varphi \hat{l}_t$ is the real wage,
* $\hat{q}_t = \hat{e}_t + \hat{p}_t^* - \hat{p}_t$ is the log real exchange rate,
* $\tilde{i}_t = i_t - i_{ss}$ is the interest rate gap,
* $\phi = \frac{\phi}{1 + \phi i_{ss}}$ is the structural cost-channel elasticity parameter.

Substituting real wages and output gap:
$$\hat{mc}_t = (\sigma + \varphi) \tilde{y}_t + \alpha \hat{e}_t + \phi \cdot \tilde{i}_t + u_t$$
where $u_t$ subsumes foreign price and productivity shocks.

---

## 3. Asymmetric Calvo Staggered Pricing

In standard Calvo (1983) pricing, a constant fraction $\theta \in (0, 1)$ of firms are unable to adjust their price in any given period, irrespective of whether the optimal desired adjustment is positive or negative.

### 3.1 The Asymmetric Pricing Mechanism
In import-dependent emerging economies with institutional frictions, monopolistic distribution tiers, and high uncertainty, firms face asymmetric menu costs and asymmetric survival constraints:
* **Upward Price Adjustment:** When cost shocks are positive ($\Delta MC_t > 0$), firms face immediate solvency risks and pass-through occurs rapidly. The probability of price rigidity is $\theta^+ \in (0, 1)$.
* **Downward Price Adjustment:** When cost shocks are negative ($\Delta MC_t < 0$), firms exploit oligopolistic market power and uncertainty buffer incentives to delay price cuts. The probability of price rigidity is $\theta^- \in (0, 1)$, where:
$$\theta^- > \theta^+ \iff (1 - \theta^-) < (1 - \theta^+)$$
*(Prices are adjusted upwards more frequently and rapidly than downwards).*

Each firm $j$ that is chosen to reset its price solves:
$$\max_{P_t^*(j)} \mathbb{E}_t \sum_{k=0}^{\infty} (\beta \theta)^k \left[ \frac{P_t^*(j)}{P_{t+k}} Y_{t+k}(j) - MC_{t+k} Y_{t+k}(j) \right]$$
subject to demand:
$$Y_{t+k}(j) = \left( \frac{P_t^*(j)}{P_{t+k}} \right)^{-\epsilon} Y_{t+k}$$
where $\epsilon > 1$ is the elasticity of substitution among intermediate goods.

### 3.2 Aggregate Inflation Dynamics under Asymmetry
The aggregate price index evolves as:
$$P_t = \left[ (1-\theta^+) (P_t^{*+})^{1-\epsilon} + (1-\theta^-) (P_t^{*-})^{1-\epsilon} + \frac{\theta^+ + \theta^-}{2} P_{t-1}^{1-\epsilon} \right]^{\frac{1}{1-\epsilon}}$$

Decomposing cost shocks into partial cumulative positive and negative sums:
$$\Delta \tilde{i}_t = \Delta i_t^+ + \Delta i_t^-, \quad \Delta \hat{e}_t = \Delta e_t^+ + \Delta e_t^-$$
where:
$$\Delta i_t^+ = \max(\Delta i_t, 0), \quad \Delta i_t^- = \min(\Delta i_t, 0)$$
$$\Delta e_t^+ = \max(\Delta e_t, 0), \quad \Delta e_t^- = \min(\Delta e_t, 0)$$

Log-linearizing the optimal pricing equations under asymmetric Calvo parameters yields the **Structural Asymmetric Cost-Channel New Keynesian Phillips Curve (ACC-NKPC)**:

$$\boxed{\pi_t = \beta \mathbb{E}_t[\pi_{t+1}] + \kappa \tilde{y}_t + \phi^+ \Delta i_t^+ + \phi^- \Delta i_t^- + \lambda^+ \Delta e_t^+ + \lambda^- \Delta e_t^- + \eta \cdot \text{Buff}_t + \varepsilon_t}$$

where the structural composite parameters are defined as:
$$\kappa = \frac{(1-\theta^+)(1-\beta \theta^+)}{\theta^+} (\sigma + \varphi)$$
$$\phi^+ = \frac{(1-\theta^+)(1-\beta \theta^+)}{\theta^+} \phi, \quad \phi^- = \frac{(1-\theta^-)(1-\beta \theta^-)}{\theta^-} \phi$$
$$\lambda^+ = \frac{(1-\theta^+)(1-\beta \theta^+)}{\theta^+} \alpha, \quad \lambda^- = \frac{(1-\theta^-)(1-\beta \theta^-)}{\theta^-} \alpha$$
$$\text{Buff}_t = \ln(FX\_Reserves_t) - \ln(FX\_Reserves_{ss})$$

---

## 4. The Threshold Lemma: Mathematical Proof of the Price Puzzle Inversion

We now formally prove why aggressive monetary tightening produces a short-run **Price Puzzle** (positive inflation response to a rate hike) in emerging markets.

### Theorem 1 (The Short-Run Price Puzzle Inversion Condition)
Let the central bank adjust the nominal policy rate by $\Delta i_t > 0$. In the short run ($t$), the net impact of the rate hike on headline inflation is:
$$\frac{\partial \pi_t}{\partial i_t} = \underbrace{\phi^+}_{\text{Cost Channel Direct Supply Shock}} - \underbrace{\frac{\kappa}{\sigma}}_{\text{Aggregate Demand Contraction Channel}}$$

### Proof:
From the dynamic IS curve:
$$\tilde{y}_t = -\frac{1}{\sigma} (i_t - \mathbb{E}_t[\pi_{t+1}])$$
Taking the derivative with respect to $i_t$:
$$\frac{\partial \tilde{y}_t}{\partial i_t} = -\frac{1}{\sigma}$$

Substituting this into the ACC-NKPC equation:
$$\pi_t = \beta \mathbb{E}_t[\pi_{t+1}] + \kappa \tilde{y}_t + \phi^+ \Delta i_t^+ + \lambda^+ \Delta e_t^+$$
Differentiating with respect to $i_t$ for $\Delta i_t > 0$:
$$\frac{\partial \pi_t}{\partial i_t} = \kappa \left( \frac{\partial \tilde{y}_t}{\partial i_t} \right) + \phi^+ = \phi^+ - \frac{\kappa}{\sigma}$$

Therefore:
$$\frac{\partial \pi_t}{\partial i_t} > 0 \iff \phi^+ > \frac{\kappa}{\sigma}$$

$$\blacksquare$$

### Economic Corollary 1.1:
In an emerging economy with high corporate working-capital bank dependence ($\phi \gg 0$) and rapid upward price adjustment ($\theta^+ \ll 1$), $\phi^+$ strictly exceeds $\frac{\kappa}{\sigma}$ in the short run. 
Consequently:
1. **Short Run ($0 \le t \le 4$ months):** $\frac{\partial \pi_t}{\partial i_t} > 0$ (Rate hikes raise marginal costs and spike headline CPI, producing the empirical Price Puzzle).
2. **Medium-to-Long Run ($t > 6$ months):** Aggregate demand contracts ($\tilde{y}_t < 0$), expectations anchor ($\mathbb{E}_t[\pi_{t+1}] \downarrow$), and the standard disinflationary mechanism reasserts dominance.

---

## 5. Summary of Testable Empirical Hypotheses

| Hypothesis | Mathematical Formulation | Economic Interpretation |
| :--- | :---: | :--- |
| **$H_1$: Asymmetric Cost Channel** | $\phi^+ > \phi^- \ge 0$ | Interest rate hikes increase marginal cost and inflation more than rate cuts reduce them. |
| **$H_2$: Asymmetric Pass-Through** | $\lambda^+ > \lambda^- > 0$ | Currency depreciation shocks pass through to CPI faster and more fully than appreciations. |
| **$H_3$: Threshold Inversion** | $\phi^+ > \frac{\kappa}{\sigma}$ at $i_t > i^*$ | When policy rates exceed critical threshold $i^*$, short-run price puzzle manifests. |
| **$H_4$: Reserve Buffer Mitigation** | $\eta < 0$ | High foreign exchange reserve buffers structurally dampen pass-through elasticity. |
