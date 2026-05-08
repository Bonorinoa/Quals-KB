# ASU Macro Qual Module Manifest

## Purpose

Use this manifest with `SKILL.md` (PhD Qual Lecture Notes Builder) to create the ASU Macro Theory PhD qualifier lecture-note system. The Macroeconomic Qualifier Playbook already exists as a compact exam reference. The module packets created from this manifest should be deeper learning documents: self-contained, derivation-heavy, exercise-rich, and directly tied to past ASU Macro qualifying exams and current course problem sets.

The goal is first-round pass preparation. Every packet should help the student recognize a problem archetype, set it up correctly, derive the key equations, exploit closed forms, avoid traps, and practice targeted variants.

## Locked Module List

Create the following six core modules before any optional extensions.

1. Optimization and Dynamic Programming.
2. OLG Model.
3. Asset Pricing Theory.
4. Search Theory.
5. Sequential, Time-0, Recursive Competitive Equilibria, and Planner/Efficient Equilibria.
6. Galina Closed-Form and Creative Dynamic Problems Lab.

Recursive Contracts is deferred. It is fair game, but it should be treated as an optional Module 7 only after the six core modules are complete.

## Repository Root and Source Folders

Primary repo path:

```text
Bonorinoa/Quals-KB/Macroeconomics/
```

Core source folders:

```text
Macroeconomics/Galina/
Macroeconomics/OLG/
Macroeconomics/Asset Pricing/
Macroeconomics/Search Theory/
Macroeconomics/RCE/
Macroeconomics/MacroQuals_2016-24/
Macroeconomics/Recursive Contracts/   # deferred until later
```

Core textbooks for reference:

```text
Ljiunsvist-Sargent "recursive macroeconomic theory"

Stokey-Lucas-Prescott "recursive methods for economic dynamics"
```

If both `.tex` and `.pdf` versions exist for a source, prefer `.tex` for text extraction and mathematical accuracy. Use PDFs when the PDF is the only available source or when diagrams/layout matter. If a source is a Mathpix conversion, check equations for conversion errors before relying on them.

## Source Hierarchy for ASU Macro

When writing any macro packet, use this source hierarchy:

1. Past ASU Macro qualifying exams from 2016-2024.
2. Current 2026 problem sets.
3. Professor lecture notes and slides.
4. Homeworks.
5. External references only when needed for clarity, rigor, or missing theory.

Past exams determine exam relevance. Problem sets determine current emphasis. Professor notes determine notation and course framing. Homeworks determine practice style.

## Current Problem Set Anchors

Use these current-course anchors when creating or auditing module packets.

### PS1: Dynamic Programming

Relevant modules: Module 1 and Module 6.

Core skills:

- mapping a problem into `v(x)=max_{y in Gamma(x)} {F(x,y)+ beta v(y)}`;
- static optimization with quadratic costs;
- finite-horizon induction;
- infinite-horizon Bellman equations;
- guess-and-verify;
- tree-cutting and stopping;
- contraction mapping;
- bounded state restrictions;
- stochastic optimal growth;
- strict concavity, monotonicity, continuity, and single-valued policies.

### PS2: Asset Pricing

Relevant module: Module 3.

Core skills:

- recursive household problem with a tree in fixed supply;
- FOC and envelope condition;
- stochastic Euler equation evaluated in equilibrium;
- Markov dividends and Markov tax states;
- log utility pricing equations;
- CRRA deterministic dividend growth;
- price-growth comparative statics;
- expected return comparisons to `1/beta`;
- war-risk pricing and risk-aversion comparisons.

### PS3: Search

Relevant module: Module 4.

Core skills:

- McCall search with probability of no offer;
- reservation-wage proof;
- state-independent versus state-dependent reservation wages;
- stochastic unemployment benefits;
- two consecutive wage offers and recall;
- temporary jobs;
- iid versus Markov aggregate states;
- ranking reservation wages through option values.

### PS4: Recursive Competitive Equilibrium

Relevant module: Module 5.

Core skills:

- RCE with inelastic labor and idiosyncratic taste shocks;
- explicit law of motion for distributions;
- whether aggregate `K` alone is a sufficient state;
- skilled and unskilled workers;
- tradable versus nontradable home good;
- sector-specific human capital;
- heterogeneous firms with sector switching costs;
- equilibrium definitions with individual states, aggregate states, prices, policies, and market clearing.

## Past Qual Pattern Anchor

Use the past exams as the empirical backbone. The repeated exam commands are:

- formulate recursively;
- derive FOC and envelope;
- derive Euler equation;
- evaluate Euler equation at equilibrium allocations and prices;
- define sequential, time-0, recursive, or stationary equilibrium;
- write law of motion for capital-labor ratio;
- write law of motion for the distribution;
- prove reservation-wage or cutoff form;
- guess and verify a closed-form policy;
- evaluate an Economist X claim formally and intuitively.

The highest-frequency historical topic is OLG. Dynamic programming/growth and asset pricing are also high-yield. RCE and search are especially important because they are prominent in current problem sets.

## Global Notation Conventions

The following are recommendations, the only important thing is to be consistent. 

### Time and Discounting

```tex
\beta \in (0,1)
```

Use `t` for calendar time. Use primes for next-period variables in recursive problems when compactness helps.

### Capital and Labor

```tex
K_t = \text{aggregate capital}, \qquad k_t = K_t/L_t
```

Use `h_t` for hours worked and `ell_t` for leisure when both appear. Avoid using `l` ambiguously.

### Returns and Prices

Use gross returns:

```tex
R_{t+1}=1+r_{t+1}
```

For firm prices in production economies:

```tex
w_t=F_L(K_t,L_t), \qquad R_{t+1}=1-\delta+F_K(K_{t+1},L_{t+1}).
```

### Recursive Equilibrium

Use:

```tex
x = \text{individual state}, \qquad S = \text{aggregate state}, \qquad \mu = \text{distribution over individual states}.
```

Distribution laws should be written in measurable-set form when possible:

```tex
\mu'(B)=\int_X \Pr\{G_x(x,\varepsilon',S)\in B \mid x,S\}\,d\mu(x).
```

### Asset Pricing

Use:

```tex
p(z) = \text{ex-dividend asset price}, \qquad d(z)=\text{dividend}, \qquad q(z)=\text{bond price}.
```

Stochastic discount factor:

```tex
M(z,z')=\beta \frac{u'(c')}{u'(c)}.
```

### OLG

Use:

```tex
c_{1t}=\text{young consumption}, \quad c_{2,t+1}=\text{old consumption}, \quad s_t=\text{savings}.
```

Generic log savings rule:

```tex
s_t=\frac{\beta}{1+\beta}e_{1t}-\frac{1}{1+\beta}\frac{e_{2,t+1}}{R_{t+1}}.
```

## Required Packet-Level Output

Each module packet should produce, at minimum:

1. `Module_X_[Short_Name].tex` (Overleaf-ready)
2. A source inventory section inside the packet.
3. A module map table.
4. Full derivations of canonical models.
5. Closed-form catalog.
6. Exam variations.
7. Common traps.
8. Exercise bank.
9. Answer sketches.
10. Past-qual practice map.
11. Final study checklist.

Recommended file names:

```text
ASU_Macro_Module_1_Optimization_DP.tex
ASU_Macro_Module_2_OLG.tex
ASU_Macro_Module_3_Asset_Pricing.tex
ASU_Macro_Module_4_Search.tex
ASU_Macro_Module_5_Equilibrium_RCE_Planner.tex
ASU_Macro_Module_6_Galina_Lab.tex
```

## Module 1: Optimization and Dynamic Programming

**Purpose**: This is the mathematical foundation packet. It should teach the core optimization and dynamic programming tools needed for every other macro module.

### Primary Source Folders

```text
Macroeconomics/Galina/
Macroeconomics/MacroQuals_2016-24/
```

Relevant current problem set:

```text
PS1: Dynamic Programming
```

### Must Cover

#### Static Optimization

- unconstrained FOC;
- constrained optimization;
- Lagrangians;
- KKT conditions;
- complementary slackness;
- concavity versus convexity;
- when FOCs are necessary versus sufficient;
- multiplier interpretation;
- envelope theorem;
- comparative statics through implicit differentiation.

#### Dynamic Programming Theory

- sequential versus recursive formulation;
- state variables and control variables;
- feasible correspondences;
- Bellman equation;
- finite horizon backward induction;
- infinite horizon stationary Bellman equations;
- deterministic DP;
- stochastic DP;
- contraction mapping theorem;
- Blackwell sufficient conditions;
- bounded dynamic programming and state-space restrictions;
- monotonicity and concavity of value functions;
- single-valued and continuous policy functions;
- FOC, envelope, Euler workflow;
- proof/argument for recursivity from payoff separability and Markov state transitions.

#### Macro Applications

- cake-eating;
- optimal growth;
- stochastic growth;
- growth with leisure;
- stopping/tree-cutting;
- quadratic reaching-the-center problem.

### Required Derivations

Include at least:

1. KKT template with economic interpretation of multipliers.
2. Bellman derivation from a sequential problem.
3. FOC-envelope-Euler derivation for standard optimal growth.
4. Bounded-state argument for stochastic growth.
5. Guess-and-verify example.
6. Proof sketch for value-function concavity and monotone policy.

### Exercise Section

Include drills on:

- setting up Lagrangians;
- identifying states and controls;
- mapping a problem into abstract DP notation;
- proving contraction;
- deriving Euler equations;
- verifying a quadratic or log value-function guess;
- proving monotonicity/concavity.

## Module 2: OLG Model

### Purpose

This packet covers Gustavo's OLG material plus every high-yield OLG mutation from past quals.

### Primary Source Folders

```text
Macroeconomics/OLG/
Macroeconomics/MacroQuals_2016-24/
```

Use Solow/growth facts only as needed to support OLG growth dynamics.

### Must Cover

- Solow background needed for capital-labor laws;
- two-period OLG;
- three-period OLG;
- lifetime budgets;
- log-utility savings rules;
- aggregation of savings;
- population growth;
- effective labor normalization;
- Cobb-Douglas wages and returns;
- steady states;
- dynamic efficiency;
- pay-as-you-go Social Security;
- old-age endowments;
- public infrastructure;
- skilled/unskilled labor;
- college/non-college labor profiles;
- home production;
- household participation thresholds;
- balanced growth with market and home goods.

### Required Derivations

Include at least:

1. General two-period log savings rule with old-age income.
2. Capital-labor law with population growth.
3. Cobb-Douglas steady state.
4. Social Security saving and pension formula.
5. OLG endowment economy interest-rate clearing.
6. Home production time allocation.
7. Participation threshold under log utility.
8. Dynamic efficiency comparison.

### Exercise Section

Include drills on:

- solving household lifetime budgets;
- aggregating savings;
- deriving `k_{t+1}` laws;
- solving steady states;
- comparing returns;
- identifying total versus per-worker effects;
- evaluating Economist X claims.

## Module 3: Asset Pricing Theory

### Purpose

This packet covers Natalia's asset-pricing material and the Lucas-tree/SDF toolkit needed for past exams and PS2.

### Primary Source Folders

```text
Macroeconomics/Asset Pricing/
Macroeconomics/MacroQuals_2016-24/
```

Relevant current problem set:

```text
PS2: Asset Pricing
```

### Must Cover

- recursive household problem with assets;
- fixed asset supply;
- ex-dividend pricing timing;
- FOC and envelope;
- stochastic Euler equation;
- stochastic discount factor;
- one-tree Lucas economy;
- two-tree Lucas economies;
- Markov dividends;
- iid dividends and log utility;
- taxes and rebates;
- deterministic dividend growth;
- CRRA pricing;
- war/disaster risk;
- bonds and risk-free rates;
- bond-in-utility or liquidity value if relevant;
- expected returns and equity premia.

### Required Derivations

Include at least:

1. Generic asset-pricing Euler equation.
2. One-tree log closed form.
3. Two-tree constant aggregate consumption result.
4. Markov tax-state pricing equations.
5. CRRA growing-dividend price-dividend ratio.
6. War-risk before/after price comparison.
7. Bond price and risk-free return.

### Exercise Section

Include drills on:

- writing household recursive problems;
- deriving FOC/envelope/Euler;
- imposing equilibrium;
- guessing log prices;
- comparing prices across tax/persistence states;
- computing expected returns.

## Module 4: Search Theory

### Purpose

This packet covers Natalia's search material and reservation-wage methods.

### Primary Source Folders

```text
Macroeconomics/Search Theory/
Macroeconomics/MacroQuals_2016-24/
```

Relevant current problem set:

```text
PS3: Search
```

### Must Cover

- McCall search;
- risk-neutral and risk-averse variants if present;
- probability of no offer;
- iid versus Markov states;
- stochastic unemployment benefits;
- reservation-wage proof;
- comparative statics of reservation wages;
- two consecutive offers;
- recall;
- temporary jobs;
- search with assets and stationary RCE if relevant from past exams;
- timing diagrams.

### Required Derivations

Include at least:

1. Basic McCall Bellman equation.
2. Reservation wage proof.
3. State-independent reservation wage under iid arrival-state averaging.
4. Reservation wages with stochastic benefits.
5. Two-offer/recall strategy description.
6. Temporary-job Bellman equations under iid and Markov aggregate states.
7. Search-with-assets cutoff if included.

### Exercise Section

Include drills on:

- writing timing-correct Bellmans;
- proving cutoff form;
- ranking reservation wages;
- proving comparative statics;
- distinguishing employment starting today versus next period;
- explaining recall behavior.

## Module 5: Sequential, Time-0, Recursive CE, and Planner/Efficient Equilibria

### Purpose

This packet covers equilibrium concepts, welfare, planner problems, recursive competitive equilibrium, and explicit distribution laws.

### Primary Source Folders

```text
Macroeconomics/RCE/
Macroeconomics/MacroQuals_2016-24/
```

Relevant current problem set:

```text
PS4: Recursive Competitive Equilibria
```

### Must Cover

- sequential competitive equilibrium;
- time-0 Arrow-Debreu equilibrium;
- recursive competitive equilibrium;
- stationary recursive competitive equilibrium;
- representative-agent planner problems;
- Pareto weights and Pareto efficiency;
- constrained efficiency;
- welfare theorem logic;
- missing markets;
- externalities;
- taxes and wedges;
- government budgets;
- aggregate state variables;
- distribution laws;
- heterogeneous agents;
- tradable versus nontradable home goods;
- sector-specific human capital;
- heterogeneous firms and switching costs.

### Required Derivations and Templates

Include at least:

1. Sequential CE definition template.
2. Time-0 CE definition template.
3. RCE definition template.
4. Stationary RCE definition template.
5. Explicit law of motion for a distribution.
6. Planner problem template.
7. CE versus planner wedge comparison.
8. Pareto efficiency/constrained efficiency explanation.
9. RCE examples for inelastic labor, skilled/unskilled types, home production, sector-specific human capital, and heterogeneous firms.

### Exercise Section

Include drills on:

- listing equilibrium objects;
- identifying individual and aggregate states;
- writing distribution laws;
- checking market clearing;
- deciding whether aggregate `K` is sufficient;
- comparing tradable and nontradable goods;
- identifying wedges and efficiency failures.

## Module 6: Galina Closed-Form and Creative Dynamic Problems Lab

### Purpose

This is not a normal lecture-note packet. It is a problem-solving lab focused on creative dynamic problems and closed-form derivations, especially OGM/cake-eating-style questions.

### Primary Source Folders

```text
Macroeconomics/Galina/
Macroeconomics/MacroQuals_2016-24/
```

Relevant current problem set:

```text
PS1: Dynamic Programming
```

### Must Cover

- cake-eating;
- OGM finite horizon;
- OGM infinite horizon;
- reaching-the-center quadratic problem;
- tree-cutting and stopping;
- natural resource extraction;
- AK models;
- disaster-risk savings;
- human capital accumulation;
- project choice with survival probability;
- management-rights/alternating-control problems;
- coefficient matching;
- choosing the right state variable;
- guessing value-function forms;
- verifying feasibility and uniqueness.

### Required Structure

For each pattern, use:

1. Recognition clues.
2. State and Bellman.
3. Candidate guess.
4. FOC and coefficient matching.
5. Policy rule.
6. Verification checklist.
7. Practice variants.

### Required Worked Examples

Include at least:

1. Quadratic reaching-the-center.
2. Cake-eating/log resource allocation.
3. Log Cobb-Douglas growth.
4. AK log growth.
5. Natural resource extraction.
6. Disaster-risk AK model.
7. Human capital investment with linear policy.
8. Project choice cutoff.

### Exercise Section

This module should have more exercises than other modules. Include:

- short guess-the-state drills;
- guess-the-value-function drills;
- coefficient-matching drills;
- closed-form policy derivations;
- proof sketches for uniqueness/monotonicity;
- past-qual-style creative problems.

## Optional Module 7: Recursive Contracts and Dynamic Insurance

Defer this module until the six core modules are complete.

### Purpose

Cover fair-game but lower-priority material that remains fresh from the recent final exam.

### Source Folder

```text
Macroeconomics/Recursive Contracts/
```

### Likely Topics

- promised utility as a state variable;
- limited commitment;
- participation constraints;
- incentive compatibility;
- asymmetric information;
- dynamic insurance;
- optimal unemployment insurance;
- recursive contracts.

## Global Exercise Bank Standards

Each full module must include exercises in four categories:

1. Mechanical drills.
2. Closed-form/proof drills.
3. Past-qual applications.
4. Trap/economist-claim questions.

Answer sketches must be included. Full solutions are optional unless requested.

## Global Quality Gates

Before considering any module complete, verify:

1. The source inventory is explicit.
2. The module map is included.
3. The packet is self-contained.
4. Canonical derivations are complete.
5. Current problem-set emphasis is reflected.
6. Past-qual mappings are included.
7. Closed forms are derived by guess-and-verify.
8. Exercises are targeted and labeled by skill.
9. Common traps are explicit.
10. TeX math is readable.
11. No long paragraphs are placed inside display math.
12. The packet does not duplicate the methodology playbook unnecessarily.

## Prompt Templates for Parallel Sessions

### Module 1 Test Prompt

```text
Use the PhD Qual Lecture Notes Builder Skill and the ASU Macro Manifest.
Create Module 1: Optimization and Dynamic Programming.
Source folder: Macroeconomics/Galina/ plus PS1 and relevant past quals.
Output requested: source inventory, detailed blueprint, then full Overleaf-ready TeX.
Depth: exhaustive but exam-facing.
Target weakness: recursive formulation and closed-form derivations.
Do not modify the methodology playbook or other module documents.
```

### Module 2 Test Prompt

```text
Use the PhD Qual Lecture Notes Builder Skill and the ASU Macro Manifest.
Create Module 2: OLG Model.
Source folder: Macroeconomics/OLG/ plus MacroQuals_2016-24.
Output requested: source inventory, detailed blueprint, then full Overleaf-ready TeX.
Depth: exhaustive but exam-facing.
Target weakness: aggregation, capital-labor laws, and comparative statics.
Do not modify the methodology playbook or other module documents.
```

## Final Harmonization Plan

After Module 1 and Module 2 are drafted, evaluate them before creating Modules 3-6.

Audit criteria:

1. Did the Skill produce consistent structure across both modules?
2. Did the macro manifest correctly steer source use?
3. Were the notes too broad, too shallow, or appropriately exam-facing?
4. Were exercises useful for targeted practice?
5. Were closed-form derivations fully shown?
6. Was TeX formatting readable?
7. Did the model waste tokens on unnecessary summaries?
8. Did it clearly separate lecture notes from the methodology playbook?

Polish `SKILL.md` and `MACRO_MANIFEST.md` only after this test.
