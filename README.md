
[![GitHub issues](https://img.shields.io/github/issues/SemdeGroot/wDRW)](https://github.com/yourgithubusername/wDRW/issues)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## About

**wDRW** provides an implementation of a **Weighted Directed Random Walk (wDRW)** algorithm for scoring the activity of gene co-expression network modules generated using WGCNA.

By combining WGCNA topological overlap matrices (TOM) with directed random walk propagation, wDRW generates module activity scores that reflect both the **network structure** of genes and the **biological and statistical relevance ** (Log2FC and padj) of differential expression. These scores offer a network-based alternative to classical eigengene-based scoring, which do not account for the network connectivity of genes.

**Key features:**

- Computes module activity scores that integrate network topology and differential expression  
- Serves as an alternative to `moduleEigengenes`-based activity scoring 
- Compatible with WGCNA pipelines

---

## Installation

```r
# Install devtools if needed
if (!requireNamespace("devtools", quietly = TRUE))
    install.packages("devtools")

devtools::install_github("SemdeGroot/wDRW")
```

```r
library(wDRW)
```

```r
# Example inputs:
# condition_id <- "Sample123"
# module_nr <- 1
# expression_df <- read.csv(system.file("extdata", "expression_df.csv", package = "wDRW"))
# TOM <- readRDS(system.file("extdata", "TOM.rds", package = "wDRW"))
```

```r
# Compute wDRW score
# wDRW_result <- compute_wDRW_score(condition_id, module_nr, expression_df, TOM)
# print(wDRW_result)
```

## Getting started

A full workflow example is provided in the package vignette.

The vignette demonstrates:

- Preparing expression data and TOM matrix
- Generating co-expression modules
- Running `compute_wDRW_score()` on a module
- Interpreting module activity scores using 

## Links

- [GitHub repository](https://github.com/SemdeGroot/wDRW)
- [Issue tracker](https://github.com/SemdeGroot/wDRW/issues)
- [Vignette (HTML)](https://semdegroot.github.io/wDRW/articles/wDRW-vignette.html)

## Contributing

Contributions are welcome! Please open an issue in the [GitHub issue tracker](https://github.com/SemdeGroot/wDRW/issues) to discuss ideas, report bugs, or suggest improvements.

## Citation

If you use this package in your work, please cite it as:

> Sem de Groot (2025). *wDRW: Weighted Directed Random Walk Algorithm for WGCNA Module Activity Scoring*.

## License

This package is licensed under the MIT license. See the [LICENSE](LICENSE) file for details.
