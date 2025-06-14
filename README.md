
[![GitHub issues](https://img.shields.io/github/issues/SemdeGroot/wDRW)](https://github.com/yourgithubusername/wDRW/issues)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## About

**wDRW** implements the **Weighted Directed Random Walk (wDRW)** algorithm for quantifying activity of gene co-expression network modules in WGCNA pipelines.

The method integrates WGCNA topological overlap matrices (TOM) with directed random walk propagation to produce network-based module activity scores, while also accounting for statistical and biological significance of differential gene expression. These scores can serve as an alternative to classical eigengene-based module summaries, which do not integrate the network structure of genes.

**Features:**

- Computes network-based module activity scores
- Alternative to `moduleEigengenes`-based summaries
- Compatible with WGCNA pipelines

---

## Installation

```r
# Install devtools if needed
if (!requireNamespace("devtools", quietly = TRUE))
    install.packages("devtools")

devtools::install_github("yourgithubusername/wDRW")
```

```r
library(wDRW)

# Example inputs:
# condition_id <- "Sample123"
# module_nr <- 1
# expression_df <- read.csv(system.file("extdata", "expression_df.csv", package = "wDRW"))
# TOM <- readRDS(system.file("extdata", "TOM.rds", package = "wDRW"))

# Compute DRW score
# drw_result <- compute_drw_score(condition_id, module_nr, expression_df, TOM)
# print(drw_result)
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
