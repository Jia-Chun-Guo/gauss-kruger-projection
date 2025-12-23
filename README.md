# gauss-kruger-projection
Reference implementations of the Gauss–Kruger projection based on Lee’s exact method and newly derived analytical formulations.
# Gauss–Krüger Projection

This repository provides reference implementations of the Gauss–Krüger (GK) projection
based on analytic formulations derived from complex analysis, including Lee’s exact
method and two newly proposed formulations.

The code accompanies the manuscript:

> **Analytic definitions of the GK projection: a review and two new formulations**  
> *Journal of Geodesy*, under review

## Contents

- `mathematica/`  
  Mathematica notebooks implementing:
  - Lee’s exact method for the GK projection,
  - two new analytic definitions proposed in the manuscript,
  - series-based realizations for computing GK coordinates, based on the series
    approximations proposed by Guo et al. (2020) with minor transformations.

- `cpp/`  
  A minimal C++ implementation illustrating the same series-based realizations and
  serving as an independent numerical implementation for cross-checking.

## Mathematical Background

The implementations are grounded in complex analysis and the theory of elliptic
functions and elliptic integrals. They emphasize analytic definitions of the
Gauss–Krüger projection and their practical numerical realization, rather than
relying solely on descriptive accounts.

## Usage

### Mathematica

Open the notebooks in `mathematica/` and follow the commented cells to compute GK
coordinates using the series approximations proposed by Guo et al. (2020), with minor
transformations applied to the analytic definitions presented in the manuscript.

### C++

The C++ code in `cpp/` provides an independent implementation of the same series-based
realizations corresponding to Lee’s exact method and the two new analytic definitions.

## Numerical Consistency

Independent implementations in Mathematica and C++ indicate that the series-based
realizations derived from the two new definitions, as well as from Lee’s exact method,
achieve accuracy comparable to that of the Krüger–n series when truncated to the same
order, consistent with the discussion in the manuscript.

## Reproducibility

The codes provided here support the numerical statements made in the manuscript.
They are intended as reference implementations for verification and reproducibility,
rather than as optimized production software.

## License

This project is released under the MIT License.
