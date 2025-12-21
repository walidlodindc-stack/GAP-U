# GAP-U v2.0 SPEC

## 1. Core Kinetic Law
Deployment is allowed only if:

dE/dt ≤ κ · (H_eff(C) – dD*/dt)

Interpretation:
Capability may only increase if safety capacity exceeds drift.

## 2. H_eff(C): Consequence-Weighted Correction
H_eff(C) = H_raw / C_risk

Tiering:
- Text output: 1
- Code / prod config: 10
- Medical / autonomy: 100
- Critical infrastructure: 1000

## 3. D*: Worst-Case Drift Metric
D* = max(subgroup failure rates)

Slices MUST include:
- general
- protected classes
- domain groups
- adversarial slice

## 4. Provenance γ
γ = Σ(weight size × trust factor) / total size

Trust Levels:
- L0: unknown — 0.0
- L1: self-attested — 0.5
- L2: signed — 0.8
- L3: third-party audited — 1.0

## 5. Deployment Check
Pass if:
margin = κ · (H_eff – dD) – dE ≥ 0
Fail if < 0
