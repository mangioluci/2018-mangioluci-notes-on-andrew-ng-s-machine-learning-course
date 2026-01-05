# Handwritten ML Derivations (Andrew Ng / classic Coursera ML)

These are my handwritten notes from a full pass through classic “foundations of ML” material — but written the way I personally learn: **derive first, code second**.

Instead of copying slides, I re-built the machinery:
- gradients from first principles,
- matrix-form solutions (normal equation / pseudo-inverse),
- vectorized implementations,
- and the full backprop + gradient-checking loop.

If you’re scanning for *math comfort*, this repo is essentially a trail of “I can do the derivations, not just run the library.”

---

## Verified performance signal

- **Coursera credential:** `QGXFU3W83HSD`
- **Final grade:** **98.4%**
- Verification link: https://www.coursera.org/account/accomplishments/verify/QGXFU3W83HSD

---

## What’s inside (by file)

### `mangioluci-s-notes-pt1.pdf` (24 pages) — Supervised learning core
**Linear regression**
- Cost function \(J(\theta)\), partial derivatives, gradient descent update rules
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
- Error terms \(\delta\) and vectorized gradient accumulation
- Parameter “unrolling” for optimizer interfaces

**Gradient checking**
- Finite differences to validate analytic gradients

**Initialization**
- Symmetry breaking via random init (why zeros fail)

**Bias/variance & model selection**
- Train/val/test split reasoning
- Learning curves and what to change when bias vs variance dominates

---

## A note on rigor (what I did beyond “completing the course”)

I wrote out **every formula derivation the instructor left as an exercise** — not as “hand-wavy intuition,” but as full symbolic steps.  
You’ll see repeated patterns that recruiters usually only get from strong math training:

- derivations of gradients from the objective,
- careful handling of vector/matrix shapes,
- chain-rule bookkeeping through multi-layer networks,
- and numerical gradient checking as a sanity test.