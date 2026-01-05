# Handwritten Machine Learning Math Derivations (based on Andrew Ng / classic Coursera ML)

These are my handwritten notes from a full pass through classic “foundations of ML” material — but written the way I personally learn: **understanding the math from the core out**.

---

## Verified performance signal

- **Coursera credential:** `QGXFU3W83HSD`
- **Final grade:** **98.4%**
- Verification link: https://www.coursera.org/account/accomplishments/verify/QGXFU3W83HSD

---

> Note: Throughout these notes, I wrote out **all the formula demonstrations/proofs that the professor left to students** (the “show that…” steps), instead of skipping them.

## What’s inside
- `mangioluci-s-notes-pt1.pdf`
- `mangioluci-s-notes-pt2.pdf`
- `mangioluci-s-notes.extracted.txt` (searchable text extraction)

## Topics covered (high level)
Inside the PDFs you’ll find handwritten derivations and implementation details for topics like:

- Gradient descent updates derived from partial derivatives (not “just the rule”)
- Normal equation + pseudo-inverse reasoning
- Logistic regression as **maximum likelihood** + convex loss
- Regularization math (why it works + how it changes gradients)
- Neural networks: forward propagation, **backpropagation**, gradient checking
- Vectorization patterns and **shape bookkeeping** (matrix dimensions everywhere)
- Model selection / diagnostics: bias vs variance, learning curves, tuning λ

## Language
Mixed **Portuguese** + **English** (whatever was fastest while doing the work).

## Suggested reading order
1) Start with `pt1` (foundations + early NN work)  
2) Continue to `pt2` (NN implementation details + diagnostics/model selection)

---
Intent: demonstrate **comfort with applied math**, **careful reasoning**, and **implementation-oriented thinking**.

## What’s inside (by file)

### `mangioluci-s-notes-pt1.pdf` (24 pages) — Supervised learning core
**Linear regression**
- Cost function $J(\theta)$, partial derivatives, gradient descent update rules
- Normal equation (matrix solution) and when it beats iterative methods

**Linear algebra for ML**
- Pseudo-inverse intuition and matrix identities
- Dimensional analysis (shape checks) to keep implementations correct

**Logistic regression**
- Sigmoid + decision boundaries
- Log-loss / likelihood intuition
- Vectorized gradients + practical optimization notes (e.g., second-order-ish solvers)

**Multiclass classification**
- One-vs-all setup, argmax prediction rule

**Regularization**
- L2 penalty added to objectives
- How regularization modifies gradients / equations

**Neural networks (setup)**
- Forward propagation notation
- NN cost function for multiclass + regularization

**Feature explosion intuition**
- Why polynomial feature mapping can jump to thousands of features

---

### `mangioluci-s-notes-pt2.pdf` (12 pages) — Training mechanics + diagnostics
**Backpropagation**
- Chain rule across layers
- Error terms $\delta$ and vectorized gradient accumulation
- Parameter “unrolling” for optimizer interfaces

**Gradient checking**
- Finite differences to validate analytic gradients

**Initialization**
- Symmetry breaking via random init (why zeros fail)

**Bias/variance & model selection**
- Train/val/test split reasoning
- Learning curves and what to change when bias vs variance dominates