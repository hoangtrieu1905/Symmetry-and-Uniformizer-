# Symmetry and Uniformizer: Powers of (1 − ζₚ)

**2025 Summer Research — Hoang Trieu & Dr. Brooke Randazzo (Augustana College)**

---

## Overview

This project investigates the algebraic structure of powers of the *uniformizer* `(1 − ζₚ)` in the cyclotomic field **ℚ(ζₚ)**, where `ζₚ` is a primitive *p*-th root of unity and *p* is an odd prime. The uniformizer `(1 − ζₚ)` generates the unique prime ideal above *p* in the ring of integers **ℤ[ζₚ]**, making it a central object in algebraic number theory and *p*-adic analysis.

The core question: **What are the explicit coefficients when `(1 − ζₚ)ⁿ` is expressed in the power basis `{1, ζₚ, ζₚ², …, ζₚᵖ⁻²}`?**

---

## Hoang's Conjecture

The research proposes and numerically validates a closed-form formula for the coefficient `cⱼ,ₙ` of `ζₚʲ` in the expansion of `(1 − ζₚ)ⁿ`:

$$c_{j,n} = \sum_{k=0}^{\lfloor n/p \rfloor} \left[ \binom{n}{j+pk}(-1)^{j+pk} - \binom{n}{p(k+1)-1}(-1)^{p(k+1)-1} \right]$$

This combinatorial formula exploits the minimal polynomial of `ζₚ` (i.e., the relation `1 + ζₚ + ζₚ² + ⋯ + ζₚᵖ⁻¹ = 0`) to reduce the full binomial expansion modulo the cyclotomic ideal.

---

## Methods

Three independent computational approaches are implemented and compared:

| Approach | Description |
|---|---|
| **Recursive** | Mutual recursion on `c₀` and `c₁` for the *p* = 2 case; exponential time |
| **Combinatorial** | Direct evaluation of the conjecture's closed-form sum; polynomial time |
| **Trigonometric** | An alternative conjectured formula using products of sine and cosine; closed-form |

A **Big O analysis** section benchmarks all three methods, showing the combinatorial and trigonometric approaches dramatically outperform the naive recursive one for large *n*.

---

## Contents

| File | Description |
|---|---|
| `Official_Notebook_for_Root_of_Unity_Research.ipynb` | Main Jupyter notebook: data enumeration, prime-factorization of coefficients, trig formula, and runtime benchmarks |
| `ISMAA_Final.pdf` | Conference presentation slides (Illinois Section of the MAA, 2025) |

---

## Key Topics

- Cyclotomic fields and rings of integers
- *p*-adic valuation of binomial-coefficient sums
- Uniformizers and ramification in algebraic number theory
- Combinatorial and trigonometric identities for roots of unity
- Computational number theory and algorithm complexity

---

## Dependencies

The notebook runs on **Python 3** with the following libraries:

```
numpy
scipy
pandas
matplotlib
seaborn
```

It was developed in **Google Colab** and uses the `google.colab.sheets` integration for interactive data viewing.

---

## Getting Started

```bash
# Clone the repository
git clone https://github.com/hoangtrieu1905/Symmetry-and-Uniformizer-.git
cd Symmetry-and-Uniformizer-

# Open the notebook (locally)
jupyter notebook "Official_Notebook_for_Root_of_Unity_Research.ipynb"
```

Or open directly in Google Colab by uploading the `.ipynb` file.

---

## Acknowledgements

This research was conducted under the supervision of **Dr. Brooke Randazzo** at **Augustana College** during the summer of 2025, and was presented at the **Illinois Section of the Mathematical Association of America (ISMAA) 2025** annual meeting.
