# Calculus & Gradients — FAANG-Level Lab

**Goal:** Become fluent with derivatives/gradients used in ML: chain rule, Jacobians, Hessians, and checking gradients numerically.

**Outcome:** Students can derive and implement gradients for common losses, and debug gradient bugs using finite differences.

---

# How to Start

1. **Fork** this repository.  
2. Open `calculus_student_lab.ipynb` in **Google Colab**.  
3. Complete all **TODO** sections.  
4. **Restart runtime → Run All** cells.  
5. Push changes and submit a **Pull Request**.  

⚠️ **Do NOT edit notebooks directly on GitHub.**

---

## Lab Rules (FAANG Style)

- ✅ Always specify shape of gradient
- ✅ Verify gradients with finite differences
- ✅ Prefer stable implementations

---

# Notebook Rules

- Do **NOT** rename the notebook  
- Do **NOT** delete TODOs  
- Do **NOT** hardcode outputs  
- Notebook must run **top-to-bottom**  

---

# Dataset

- Synthetic vectors/matrices only

## Why?

- Removes data distractions
- Forces focus on math + implementation correctness

---

## Section 1 — Finite Differences (Gradient Checking)

### Task 1.1: Numerical gradient for scalar function f(w)

Implement central difference gradient.

**Checkpoint Questions:**

- Why is central difference more accurate than forward difference?
- What happens if `eps` is too small or too large?

**Interview Angle:**

- How would you debug an autodiff bug in production?

---

## Section 2 — Chain Rule in Code

### Task 2.1: MSE loss + gradient for linear regression

Implement loss and gradient and verify with numerical gradient.

**FAANG Gotcha:**

- Most gradient bugs are shape bugs (broadcasting) or missing constants.

---

## Section 3 — Logistic Regression Gradient (Core Interview)

### Task 3.1: BCE loss + gradient

Implement sigmoid + binary cross-entropy loss/grad.

**Checkpoint Questions:**

- Why does the gradient simplify to `X^T(p-y)/n`?
- Why must you clip probabilities for numerical stability?

---

## Section 4 — Jacobian/Hessian Intuition

### Task 4.1: Numerical Hessian for simple function

Compute Hessian numerically and compare to closed form.

**Interview Angle:**

- What does the Hessian tell you about optimization and curvature?

---

## Stretch

- Derive logistic regression gradient (vectorized)
- Implement softmax + cross-entropy gradient

---

## Submission Expectations

Students must submit:

- Clean notebook (runs top-to-bottom)
- Gradient checks passing
- Short answers for **Checkpoint/Explain** prompts

---

## FAANG Interview Evaluation Rubric

| Skill                     | Evaluated |
|---------------------------|-----------|
| Gradient correctness       | ✅        |
| Numerical stability        | ✅        |
| Shape reasoning            | ✅        |
| Debugging discipline       | ✅        |
| Explanation clarity        | ✅        |
