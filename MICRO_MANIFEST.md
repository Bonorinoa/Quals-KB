# ASU Micro Qual Module Manifest

## Purpose

Use this manifest with `SKILL.md` (PhD Qual Lecture Notes Builder) to create the ASU Micro Theory PhD qualifier lecture-note system. The Microeconomics Qualifier Playbook (38 pages, 2013–2024 patterns) already exists as the compact exam reference. The module packets created from this manifest should be deeper learning documents: self-contained, derivation-heavy, exercise-rich, and directly tied to past ASU Micro qualifying exams and the universal proof moves, prototypes, and traps documented in the playbook.

The goal is first-round pass preparation. Every packet must help the student recognize an exam archetype instantly, write the four-layer answer (Object → Feasibility → Optimality/Equilibrium → Verification), exploit the 25 reusable templates, avoid the 15 common traps, and practice the exact high-yield proof moves (revealed-preference addition, single-crossing monotonicity, envelope, Bayes consistency, zero-profit, etc.).

## Locked Module List

Create the following six core modules before any optional extensions.

1. Consumer Theory, Demand, and Comparative Statics  
2. General Equilibrium, Excess Demand, and Welfare Theorems  
3. Static Games, Extensive-Form Games, and Repeated/OLG Games  
4. Bayesian Games, Signaling, and Verifiable Disclosure  
5. Screening, Adverse Selection, Insurance, and Credit  
6. Moral Hazard, Principal-Agent, and Mechanism Design (including Auctions)

Decision Theory/Uncertainty (SEU, state-contingent Edgeworth boxes, testable implications) is distributed across Modules 1–2 and treated as a cross-cutting skill rather than a standalone module.

## Repository Root and Source Folders

```text
Bonorinoa/Quals-KB/Microeconomics/
```

Core source folders:  

```text
Microeconomics/MicroQuals_2013-24/
Microeconomics/*
```

Core textbooks for reference:

```text
MasCollel-Whinston-Green "microeconomic theory"

Kreps "advanced microeconomic theory"
```

If both `.tex` and `.pdf` exist, prefer `.tex` for equations. Use the attached playbook as the primary pattern anchor for every module.

## Source Hierarchy for ASU Micro

1. Past ASU Micro qualifying exams (2013–2024) — determine exam relevance and archetype frequency.  
2. Current 2026 problem sets (if supplied).  
3. MWG / Kreps textbook excerpts — supply rigor and notation when the playbook is silent.  
4. Professor lecture notes and slides
5. External references only when needed for clarity, rigor, or missing theory.

## Current Problem-Set Anchors 

- Fall core (demand, partial eqm, static games) → Modules 1 & 3  
- Spring core (Bayesian, signaling, screening, moral hazard, mechanism design) → Modules 4, 5, 6  
- Cross-cutting: revealed-preference arguments, single-crossing monotonicity, envelope moves, zero-profit + IC/IR binding logic, off-path belief construction.

## Global Notation Conventions

The following are recommendations, the only important thing is to be consistent. 

- Budget set: \( B(p, w) = \{ x \in X : p \cdot x \leq w \} \)  
- Walrasian demand: \( d(p, w) \) (correspondence) or \( x(p, w) \) (function)  
- Indirect utility: \( V(p, w) \); expenditure: \( e(p, \bar{u}) \)  
- Excess demand: \( z(p) = \sum_i (x_i(p, p \cdot \omega_i) - \omega_i) \)  
- IC/IR: \( U_i(c_i) \geq U_i(c_j) \), \( U_i(c_i) \geq \bar{U}_i \)  
- MLRP / FOA in moral hazard  
- Beliefs \( \mu \), assessments \( (\sigma, \mu) \) in sequential equilibrium  
- Virtual value in mechanism design (Myerson)  
- Use primes for next-period or continuation values; subscripts for types (L/H or i).

## Required Packet-Level Output (identical to Macro)

Each module packet must contain, at minimum:

1. `ASU_Micro_Module_X_[Short_Name].tex` (Overleaf-ready)  
2. Source inventory section  
3. Module map table (subtopic → why it matters → playbook prototype → core technique → common trap)  
4. Full derivations of canonical models with four-layer answer template   
6. Exam variations (how the archetype mutates on 2013–2024 quals)  
7. Common traps 
8. Exercise bank (30 % mechanical, 30 % proof/characterization, 25 % past-qual application, 15 % trap/“Economist X” claim)  
9. Answer sketches (concise 3–5 line solutions)  
10. Past-qual practice map (exact year/Q# references)  
11. Final study checklist

Recommended file names:  

```text
ASU_Micro_Module_1_Consumer_Demand.tex  
ASU_Micro_Module_2_Decision_Uncertainty.tex
ASU_Micro_Module_3_GE_Welfare.tex  
ASU_Micro_Module_4_Static_Extensive_Games.tex  
ASU_Micro_Module_5_Bayesian_Signaling.tex
ASU_Micro_Module_6_Screening_Adverse_Selection.tex
ASU_Micro_Module_7_Moral_Hazard_Mechanism.tex
```

## Module 1: Consumer Theory, Demand, and Comparative Statics

**Purpose**: Master the four-layer answer for quasilinear demand, KKT corners, revealed-preference proofs (no-Giffen, normality), single-crossing monotonicity, value-function curvature, and endowment-choice problems.

**Primary Sources**: 2018 Q1–Q2, 2020 Q1, 2024 Q1, 2013 Q3, 2018 Q2, 2023 Q4. `https://github.com/Bonorinoa/Quals-KB/tree/main/Microeconomics/Partial%20Equilibrium`, `https://github.com/Bonorinoa/Quals-KB/tree/main/Microeconomics/Decision%20Theory`

**Must Cover**:
- Quasilinear two-good demand (budget exhaustion → one-dimensional max → corners)
- No-Giffen/normality via adding optimality inequalities (revealed-preference addition)
- KKT for nonnegative consumption + state-contingent SEU
- Indirect utility with endogenous endowment choice
- Single crossing / increasing differences / monotone selection (Topkis)
- Value function convexity (supremum of affine functions)
- Cost/profit functions and input-demand monotonicity (revealed-cost inequalities)

**Required Derivations** (show four-layer answer each time):
1. Quasilinear demand protocol + corner check
2. Adding optimality inequalities for comparative statics
3. KKT + complementary slackness for interior vs. boundary
4. Single-crossing difference-of-differences proof
5. Supremum-of-affine-functions convexity argument

**Exercise Bank** (target 12–15 items):
- Mechanical: write KKT, reduce quasilinear to 1D, compute difference-of-differences
- Proof: prove no Giffen, prove monotone selection, prove convexity of V(t)
- Past-qual: 2018 Q2, 2024 Q1, 2020 Q1 variants
- Trap: “prove every maximizer increases” vs. “there exists a maximizer that increases”

## Module 2: General Equilibrium, Excess Demand, and Welfare Theorems

**Purpose**: Master excess-demand derivation, Walras’ Law tricks, existence conditions, Edgeworth-box PO, and both Welfare Theorems with exact assumption checks.

**Primary Sources**: 2020 Q3, 2021 Q1, 2024 Q1, 2015 Q1, 2017 Q2, 2022 Q1.

**Must Cover**:
- Individual & aggregate excess demand + normalization
- Walras’ Law + missing-market clearing
- Closed-graph argument for equilibrium correspondences
- Edgeworth-box PO (MRS equalization, risk-sharing, boundary cases)
- First & Second Welfare Theorems (LNS, convexity, supporting prices, transfers)
- Robinson Crusoe / representative-firm economies

**Required Derivations**:
1. z(p) construction + Walras’ Law reduction
2. Boundary-condition existence argument
3. Direct contradiction for no-WE examples
4. KKT vs. tangency for interior vs. boundary PO
5. SFWT contradiction + SWFT support + transfer construction

## Module 3: Static Games, Extensive-Form Games, and Repeated/OLG Games

**Purpose**: Master strategy-set writing, best-reply intersections, SPNE via continuation values, sequential equilibrium assessments, and repeated/OLG incentive constraints.

**Primary Sources**: 2023 Q1, 2024 Q2, 2018 Q4, 2019 Q1, 2016 Q2.

**Must Cover**:
- Complete contingent plans (information sets, histories, types)
- Pure/mixed NE + support enumeration + off-support checks
- Weak dominance (quantify over all opponent strategies)
- SPNE by backward induction + continuation values
- Sequential equilibrium (strategies + beliefs + sequential rationality + consistency)
- Finite repetition last-period unraveling + OLG young/old incentive separation

**Required Derivations**:
1. Strategy-set construction for signaling / owner-manager / OLG
2. Mixed NE indifference + off-support inequality verification
3. Continuation-value recursion for SPNE
4. Assessment (σ, μ) + Bayes on-path + limiting perturbation off-path

## Module 4: Bayesian Games, Signaling, and Verifiable Disclosure

**Purpose**: Master BNE type-contingent best responses, WPBE construction (pooling/separating/least-cost), and verifiable-disclosure unraveling.

**Primary Sources**: 2018 Q3, 2017 Q2, 2022 Q3, 2024 Q3, 2021 Q4.

**Must Cover**:
- Bayesian Nash (interim expected payoffs, type-by-type inequalities)
- Incomplete-information Cournot (posterior beliefs, disclosure extensions)
- Signaling WPBE (sender strategy, receiver best response to beliefs, zero-profit wages)
- Least-cost separating construction (recursive no-mimic constraints)
- Pooling vs. partial pooling + off-path belief punishment
- Verifiable disclosure (type-dependent message sets, no-lying constraints, unraveling)

**Required Derivations**:
1. BNE system of interim best-response inequalities
2. Separating e_H interval from two IC inequalities
3. Zero-profit wage = E[θ | e] on path
4. Unraveling argument when high type can profitably deviate

## Module 5: Screening, Adverse Selection, Insurance, and Credit

**Purpose**: Master IC/IR menu construction, single-crossing monotonicity, binding-constraint logic, and competitive zero-profit screening existence checks.

**Primary Sources**: 2021 Q3, 2014 Q3, 2020 Q2, 2019 Q4, 2023 Q4.

**Must Cover**:
- IC/IR template + binding-constraint identification
- Insurance screening (zero-profit lines, full vs. partial coverage distortion)
- Credit screening with collateral (inefficient collateral as screening device)
- Monotone menus from strict increasing differences

**Required Derivations**:
1. Reduced system after identifying binding IR_L + IC_H
2. Rothschild-Stiglitz-style separating candidate + deviation test
3. Single-crossing proof that higher type gets weakly higher q

## Module 6: Moral Hazard, Principal-Agent, and Mechanism Design (incl. Auctions)

**Purpose**: Master MLRP/FOA validity, cost-minimizing contract under IC, virtual-value revenue maximization, and IC utility envelope characterization.

**Primary Sources**: 10.1–10.4 + 2019 Q3, 2014 Q4, 2022 Q3, 2021 Q3.

**Must Cover**:
- Baseline moral hazard (PC + global IC or FOA)
- MLRP + CDFC for FOA validity + wage monotonicity
- Cost-minimizing compensation in utility terms
- Direct revelation mechanism + envelope + monotonicity
- Myerson virtual value + revenue equivalence

**Required Derivations**:
1. FOA first-order condition + multiplier on likelihood ratio
2. IC utility envelope U'(x) = Q(x) + monotonicity requirement
3. Virtual-value allocation rule for revenue max

## Global Exercise Bank Standards

Each full module must include exercises in four categories:

1. Mechanical drills.
2. Closed-form/proof drills.
3. Past-qual applications.
4. Trap/economist-claim questions.

Answer sketches must be included. Full solutions are optional unless requested.


## Global Quality Gates 

Before any packet is considered complete, verify:
- Source inventory explicit and playbook-page references included
- Module map table present
- Four-layer answer template used in every canonical derivation
- All common traps from playbook pages 34–35 called out
- Past-qual practice map with exact year/Q# 
- Exercises target the 25 reusable templates (Appendix B)
- TeX is readable, no long paragraphs inside display math
- Packet does not duplicate the 38-page playbook — it deepens it

