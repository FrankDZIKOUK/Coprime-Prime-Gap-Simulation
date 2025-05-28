# Coprime-Prime-Gap-Simulation

Jupyter Notebook for coprime probability proof and Cramér's conjecture simulation

## Probability and Prime Number Simulation

### Overview

This project contains a Jupyter Notebook that explores a probability problem involving the selection of two integers and their coprimality, as well as a simulation related to prime gaps.

### Objectives

- **Probability of Coprime Integers:** Prove that the probability \(\mathcal{P}_n\) that two integers chosen uniformly and independently from \([1, n]\) are coprime is approximately \(\frac{6}{\pi^2}\).
- **Cramér's Conjecture Simulation:** Simulate the normalized gap between consecutive primes, \(\frac{\mathfrak{p}_{n+1} - \mathfrak{p}_n}{\log(\mathfrak{p}_n)^2}\), to investigate Cramér’s conjecture.

### Problem Description

#### Part 1: Coprime Probability

The first part of the notebook addresses the probability that two integers \(a\) and \(b\), chosen uniformly and independently from \([1, n]\), are coprime (i.e., their greatest common divisor is 1).

- Calculating the size of the sample space and the event where two integers are coprime.
- Using the principle of inclusion-exclusion to compute the number of coprime pairs.
- Applying the Möbius function and properties of the Riemann zeta function to derive the asymptotic result.

#### Part 2: Cramér's Conjecture Simulation

The second part simulates a model inspired by Cramér's conjecture, which posits that the gap between consecutive primes \(\mathfrak{p}_n\) and \(\mathfrak{p}_{n+1}\) satisfies:

\[
\limsup_{n \to \infty} \frac{\mathfrak{p}_{n+1} - \mathfrak{p}_n}{\log(\mathfrak{p}_n)^2} = 1
\]

### Code Structure

The Jupyter Notebook (`Coprime-Prime-Gap-Simulation.ipynb`) contains:

- **Theoretical Proof:**
  - Markdown cells detailing the step-by-step proof of the coprime probability.
  - Use of inclusion-exclusion and the Möbius function to compute \(\mathcal{P}_n\).
  - A lemma proving that \(\sum_{n=1}^\infty \frac{\mu(n)}{n^s} = \frac{1}{\zeta(s)}\) for \(s > 1\).

- **Simulation Code:**
  - Python code using libraries like `numpy`, `scipy`, and `matplotlib`.
  - A function `realisation_uniforme(n)` to generate uniform integers from \([0, 1]\) mapped to \([1, n]\).
  - Functions `GenerateCramerPrime(n)` and `valeurs(arr)` to simulate prime-like sequences and compute normalized prime gaps.
  - A visualization plotting the normalized gaps for \(N = 10{,}000\) over 500 iterations, with a horizontal line at \(y = 1\) to compare with Cramér's conjecture.

### Results

- **Coprime Probability:** The proof confirms that \(\mathcal{P}_n \approx \frac{6}{\pi^2} \approx 0.6079\), with an error term of \(O\left(\frac{\ln n}{n}\right)\).
- **Cramér's Simulation:** The plot shows that the normalized prime gaps \(\frac{\mathfrak{p}_{n+1} - \mathfrak{p}_n}{\log(\mathfrak{p}_n)^2}\) are mostly distributed between 0 and 2.

### Requirements

To run the notebook, you need the following Python libraries:

- `numpy`
- `scipy`
- `matplotlib`

Install them using:

```bash
pip install numpy scipy matplotlib

