# Gauss–Krüger Projection

This repository provides reference implementations of the Gauss–Krüger (GK) projection
based on analytic formulations derived from complex analysis. The implementations
cover Lee’s exact method and two newly proposed analytic definitions introduced in the
accompanying manuscript.

The emphasis of this repository is on **analytic definitions and their series-based
numerical realizations**, rather than on optimized production algorithms.

---

## Associated Manuscript

The code accompanies the manuscript:

> **Analytic definitions of the Gauss–Krüger projection: a review and two new formulations**  
> *Journal of Geodesy*, under review

---

## Repository Structure

### `mathematica/`

Mathematica notebooks implementing:

- Lee’s exact analytic definition of the GK projection,
- two newly proposed analytic definitions introduced in the manuscript,
- series-based realizations for computing GK coordinates, derived from these analytic
  definitions,
- series formulations related to the approach of Guo et al. (2020), with minor analytic
  transformations.

The notebooks are primarily intended for symbolic inspection, high-precision numerical
evaluation, and verification of analytic relations.

---

### `cpp/`

A minimal C++ implementation providing:

- independent numerical realizations of the same series-based formulations,
- cross-checks against the Mathematica implementations,
- illustrative examples for practical numerical evaluation.

The C++ code focuses on clarity and consistency with the analytic derivations, rather
than on computational efficiency or full-scale library design.

---

## Mathematical Background

The implementations are grounded in complex analysis and the theory of elliptic
integrals and elliptic functions. Instead of relying solely on descriptive or
historically motivated formulations, the code reflects explicit analytic definitions
of the Gauss–Krüger projection and examines how these definitions can be realized
numerically through series approximations.

---

## Usage

### Mathematica

Open the notebooks in the `mathematica/` directory and follow the commented cells.
The notebooks demonstrate how GK coordinates are computed using series-based
realizations derived from the analytic definitions discussed in the manuscript.

High-precision arithmetic is used where appropriate to facilitate verification and
comparison.

---

### C++

The C++ code in the `cpp/` directory implements the same series-based realizations
corresponding to Lee’s exact method and the two new analytic definitions. It serves as
an independent numerical implementation for consistency checks and reproducibility
tests.

---

## Numerical Consistency

Independent implementations in Mathematica and C++ indicate that the series-based
realizations derived from Lee’s exact method and from the two new analytic definitions
achieve accuracy comparable to that of the classical Krüger–$n$ series when truncated
to the same order, consistent with the analysis presented in the manuscript.

---

## Reproducibility and Scope

The codes provided in this repository support the numerical statements made in the
manuscript. They are intended as **reference implementations** for verification,
comparison, and reproducibility, rather than as optimized or production-ready software
for large-scale geodetic applications.

---

## License

This project is released under the MIT License.
