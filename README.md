# Handwritten ML Derivations (classic Coursera ML)

This repo is a **math-forward work sample**: handwritten derivations + implementation notes for core supervised learning and neural networks.

The point is not “I watched a course.” The point is: **I can reconstruct the machinery**—derive gradients, reason in matrix form, sanity-check with numerical approximations, and keep implementations honest with shape checks.

---

## Verified performance signal

- **Coursera credential:** `QGXFU3W83HSD`
- **Reported final grade:** **98.4%**
- Verification link: https://www.coursera.org/account/accomplishments/verify/QGXFU3W83HSD

---

## Fast proof (2-minute skim)

If you read only ~5 minutes of this repo, read these four pages in order.  
They show the full pipeline: **vectorized forward pass → vectorized inference → multiclass shape discipline → backprop math + derivative rigor**.

> Note on authorship: **p-24 contains my full derivations (including the “exercise left to the student” steps).**  
> The backprop algorithm on p-23 is included as context for the derivations on p-24.

---

### 1) Neural network forward propagation, vectorized (setup + weight semantics)
**Why it matters:** Correct \(\Theta^{(l)}\) semantics + bias handling is where implementations quietly go wrong.

![Neural net forward propagation (vectorized)](pages-11-20/mangioluci-s-notes-p-14.pdf)

---

### 2) One-vs-all inference, vectorized (probabilities → argmax)
**Why it matters:** Shows the bridge from equations to working prediction code (shape-aware, batch-friendly).

![One-vs-all prediction (vectorized argmax)](pages-11-20/mangioluci-s-notes-p-18.pdf)

---

### 3) Multiclass formulation as linear algebra (\(h(x)\in\mathbb{R}^K\), \(Y\in\mathbb{R}^{m\times K}\))
**Why it matters:** Demonstrates tensor/shape thinking—turning “K-class classification” into matrices you can actually compute with.

![Multiclass shapes and one-hot encoding](pages-21-30/mangioluci-s-notes-p-20.pdf)

---

### 4) Backprop rigor: sigmoid derivative + dimensional analysis + bias-unit caveats (**my derivation**)
**Why it matters:** This is the “engine room”: chain rule mechanics, \(g'(z)=g(z)(1-g(z))\), and explicit dimension checks that prevent subtle training bugs.

![Sigmoid derivative + backprop dimensional analysis (my derivation)](pages-21-30/mangioluci-s-notes-p-24.pdf)

---

## What’s inside

This repo stores the handwritten pages as **per-page PDFs**:

- `pages-1-10/` — `mangioluci-s-notes-p-01.pdf` … `mangioluci-s-notes-p-10.pdf`
- `pages-11-20/` — `mangioluci-s-notes-p-11.pdf` … `mangioluci-s-notes-p-20.pdf`
- `pages-21-30/` — `mangioluci-s-notes-p-21.pdf` … `mangioluci-s-notes-p-30.pdf`
- `pages-31-36/` — `mangioluci-s-notes-p-31.pdf` … `mangioluci-s-notes-p-36.pdf`

---

## Index

This index is designed for a recruiter or engineer to jump straight to “proof of math” quickly.

| Topic | What you’ll see | Where |
|------|------------------|------------------------|
| Linear Regression | Cost \(J(\theta)\), partial derivatives, gradient descent update rule, vectorization notes | p. 1–5 |
| Normal Equation | Closed-form \(\theta = (X^TX)^{-1}X^Ty\), tradeoffs vs GD | p. 5–7 |
| Pseudo-inverse | Pseudo-inverse intuition + use in least squares | p. 7–8 |
| Logistic Regression | Sigmoid, log-loss, likelihood framing, gradient derivation | p. 9–12 |
| Regularization (L2) | Adds penalty term, modifies gradients / equations | p. 12–14 |
| Multiclass (One-vs-All) | Setup + prediction via argmax | p. 14–15 |
| Neural Nets (Setup) | Forward prop notation, NN cost function, shape bookkeeping | p. 15–20 |
| Feature Explosion | Polynomial feature mapping intuition (combinatorics blow-up) | p. 20–24 |
| Backpropagation | Chain rule across layers, \(\delta\) terms, vectorized gradients | p. 25–30 |
| Parameter Unrolling | Reshaping \(\Theta\) into vectors for optimizers, gradient vectorization | p. 27–30 |
| Gradient Checking | Finite-difference approximation as sanity check | p. 30–31 |
| Random Initialization | Symmetry breaking + ranges/epsilon intuition | p. 31–32 |
| Bias vs Variance | Learning curves, diagnostics, remedies by failure mode | p. 33–36 |

---

## Rigor note (why these aren’t “just notes”)

I explicitly wrote out **all formula demonstrations that the professor left as exercises**—full symbolic steps, not hand-wavy intuition.

Recurring “advanced-math-ish” signals you’ll notice:

- gradients derived from the objective (not copied),
- careful vector/matrix shape tracking (prevents silent bugs),
- chain-rule bookkeeping through multi-layer networks,
- numerical gradient checking to validate analytic gradients,
- explicit bias/variance diagnosis patterns.

---

## How to browse quickly

1) Start with **Fast proof (2-minute skim)** above.
2) Jump to the **Index** row that matches what you care about (e.g., “regularized logistic gradient”).
3) Open the corresponding per-page PDFs (e.g., `pages-11-20/mangioluci-s-notes-p-13.pdf`).

---

## Language

Mixed **Portuguese** + **English** (whatever was fastest while doing the work).