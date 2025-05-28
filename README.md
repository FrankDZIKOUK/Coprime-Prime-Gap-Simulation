# Coprime-Prime-Gap-Simulation

Jupyter Notebook for coprime probability proof and Cramér's conjecture simulation.

## Probability and Prime Number Simulation

### Overview

This project contains a Jupyter Notebook that explores a probability problem involving the selection of two integers and their coprimality, as well as a simulation related to prime gaps.

---

### Objectives

- **Probability of Coprime Integers:** Prove that the probability ![P_n](https://latex.codecogs.com/png.latex?\mathcal{P}_n) that two integers chosen uniformly and independently from \([1, n]\) are coprime is approximately:

  ![P_n ≈ 6 / π²](https://latex.codecogs.com/png.latex?\mathcal{P}_n%20\approx%20\frac{6}{\pi^2})

- **Cramér's Conjecture Simulation:** Simulate the normalized gap between consecutive primes:

  ![(p_{n+1} - p_n) / (log(p_n))^2](https://latex.codecogs.com/png.latex?\frac{\mathfrak{p}_{n+1}%20-%20\mathfrak{p}_n}{\log(\mathfrak{p}_n)^2})

  to investigate Cramér’s conjecture.

---

### Problem Description

#### Part 1: Coprime Probability

The first part addresses the probability that two integers \(a\) and \(b\), chosen uniformly and independently from \([1, n]\), are coprime (i.e., their greatest common divisor is 1).

- Calculating the size of the sample space and the event where two integers are coprime.
- Using the principle of inclusion-exclusion to compute the number of coprime pairs.
- Applying the Möbius function and properties of the Riemann zeta function to derive the asymptotic result.

---

#### Part 2: Cramér's Conjecture Simulation

The second part simulates a model inspired by Cramér's conjecture, which posits:

![Cramér's Conjecture](https://latex.codecogs.com/png.latex?\limsup_{n\to\infty}%20\frac{\mathfrak{p}_{n+1}%20-%20\mathfrak{p}_n}{\log(\mathfrak{p}_n)^2}%20=%201)

---

### Code Structure

The Jupyter Notebook `Coprime-Prime-Gap-Simulation.ipynb` contains:

- **Theoretical Proof:**
  - Markdown cells detailing the proof of the coprime probability.
  - Use of inclusion-exclusion and Möbius function to compute ![P_n](https://latex.codecogs.com/png.latex?\mathcal{P}_n).

- **Simulation Code:**
  - Python code using `numpy`, `scipy`, `matplotlib`.
  - A function `realisation_uniforme(n)` to generate uniform integers from \([0,1]\) mapped to \([1, n]\).
  - Functions `GenerateCramerPrime(n)` and `valeurs(arr)` to simulate prime-like sequences and compute normalized prime gaps.
  - A plot showing normalized gaps for \(N = 10,000\) over 500 iterations, with a line at \(y = 1\) as reference.

---

### Results

- **Coprime Probability:** The proof confirms:

  ![Result](https://latex.codecogs.com/png.latex?\mathcal{P}_n%20\approx%20\frac{6}{\pi^2}%20\approx%200.6079)

  with an error term:

  ![Error](https://latex.codecogs.com/png.latex?O\left(\frac{\ln%20n}{n}\right))

- **Cramér's Simulation:** The normalized prime gaps

  ![Gaps](https://latex.codecogs.com/png.latex?\frac{\mathfrak{p}_{n+1}%20-%20\mathfrak{p}_n}{\log(\mathfrak{p}_n)^2})

  are mostly between 0 and 2.

---

### Requirements

To run the notebook, install:

```bash
pip install numpy scipy matplotlib
