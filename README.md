
<!-- README.md is generated from README.Rmd. Please edit that file -->
<!-- badges: start -->

[![Lifecycle:
experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://www.tidyverse.org/lifecycle/#experimental)
<!-- badges: end -->

# `deepvars`

The `deepvars` package provides a framework for Deep Vector
Autoregression in R. The methodology is based on [Altmeyer, Agusti and
Vidal-Quadras Costa
(2021)](https://github.com/pat-alt/deepvarsMacro/blob/main/paper/paper.pdf),
a working paper initially prepared as part of the [Masters Degree in
Data
Science](https://bse.eu/study/masters-programs/data-science-methodology)
at [Barcelona School of Economics](https://bse.eu). For a summary of the
first version of the working paper see
[here](https://thevoice.bse.eu/2021/09/16/deep-vector-autoregression-for-macroeconomic-data/).

<p align="center">
<img src="www/hex.png" style="width: 250px;" />
</p>

## Installation

### Prerequisites

As one of its dependencies the `deepvars` uses `tensorflow`, which is an
R interface to the popular [TensorFlow](https://www.tensorflow.org)
library. We have tried to automate the TensorFlow configuration as
explained
[here](https://rstudio.github.io/reticulate/articles/python_dependencies.html).

``` r
install.packages("tensorflow")
tensorflow::install_tensorflow()
```

For uncertainty quantification we use `tensorflow_probability` for
Bayesian inference.

``` r
install.packages("tfprobability")
tfprobability::install_tfprobability()
```

Should you run into issues you may have to manually install the
TensorFlow dependencies. Detailed instructions to this end can be found
[here](https://tensorflow.rstudio.com/installation/).

### Install

You can either clone this repository and install from source or simply
run the below in R:

``` r
devtools::install_github("pat-alt/deepvars", build_vignettes=TRUE)
library(deepvars)
```

## Getting started

Full documenation of the package is still missing. In the meantime,
detailed guidance on different topics and estimation methods covered by
`deepvars`, can be found in the vignettes. Simply type the following
command once you have completed the steps above:

``` r
utils::browseVignettes('deepvars')
```

## Citation

If you would like to cite our work in your own research, we’d much
appreciate it. Please cite this package as follows:

    @Manual{altmeyer2021deepvars,
      title = {deepvars: Deep Vector Autoregression},
      author = {Patrick Altmeyer},
      note = {R package version 0.1.0}}

Please cite the related working paper as follows:

    @article{altmeyer2021deep,
        author = {Altmeyer, Patrick and Agusti, Marc and Vidal-Quadras Costa, Ignacio},
        date-added = {2021-09-23 13:33:59 +0200},
        date-modified = {2021-11-30 16:33:49 +0100},
        title = {Deep Vector Autoregression for Macroeconomic Data},
        url = {https://thevoice.bse.eu/wp-content/uploads/2021/07/ds21-project-agusti-et-al.pdf},
        year = {2021}}
