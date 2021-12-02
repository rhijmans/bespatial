
<!-- README.md is generated from README.Rmd. Please edit that file -->

# bespatial

<!-- badges: start -->
[![R-CMD-check](https://github.com/Nowosad/bespatial/workflows/R-CMD-check/badge.svg)](https://github.com/Nowosad/bespatial/actions)
[![Lifecycle:
experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://lifecycle.r-lib.org/articles/stages.html#experimental)
[![Codecov test
coverage](https://codecov.io/gh/Nowosad/bespatial/branch/master/graph/badge.svg)](https://app.codecov.io/gh/Nowosad/bespatial?branch=master)
<!-- badges: end -->

The goal of **bespatial** is to calculate sevaral entropy metrics for
spatial data inspired by Boltzmann’s entropy formula. It includes
metrics introduced by Cushman for landscape mosaics (Cushman (2015)),
and landscape gradients and point patterns (Cushman (2021)); by Gao et
al. for landscape gradients (2017, 2019).

## Installation

<!-- You can install the released version of bespatial from [CRAN](https://CRAN.R-project.org) with: -->
<!-- ``` r -->
<!-- install.packages("bespatial") -->
<!-- ``` -->

You can install the development version from
[GitHub](https://github.com/) with:

``` r
# install.packages("remotes")
remotes::install_github("Nowosad/bespatial")
```

## Example

``` r
library(terra)
#> terra version 1.5.0
library(bespatial)
mosaic = rast(system.file("raster/mosaic.tif", package = "bespatial"))
ce1 = bes_m_cushman(mosaic, 1000)
plot(mosaic, main = round(ce1$value, 2))
```

<img src="man/figures/README-unnamed-chunk-2-1.png" width="100%" />

<!-- ## Documentation -->

## References

-   Cushman, S. A. (2015). Calculating the configurational entropy of a
    landscape mosaic. In Landscape Ecology (Vol. 31, Issue 3,
    pp. 481–489). Springer Science and Business Media LLC.
    <https://doi.org/10.1007/s10980-015-0305-2>
-   Cushman, S. (2018). Calculation of Configurational Entropy in
    Complex Landscapes. In Entropy (Vol. 20, Issue 4, p. 298). MDPI AG.
    <https://doi.org/10.3390/e20040298>
-   Cushman, S. A. (2021). Generalizing Boltzmann Configurational
    Entropy to Surfaces, Point Patterns and Landscape Mosaics. In
    Entropy (Vol. 23, Issue 12, p. 1616). MDPI AG.
    <https://doi.org/10.3390/e23121616>
-   Gao, Peichao, Hong Zhang, and Zhilin Li. “A hierarchy-based solution
    to calculate the configurational entropy of landscape gradients.”
    Landscape Ecology 32(6) (2017): 1133-1146.
-   Gao, Peichao and Zhilin Li. “Aggregation-based method for computing
    absolute Boltzmann entropy of landscape gradient with full
    thermodynamic consistency.” Landscape Ecology (2019).

## Contribution

Contributions to this package are welcome - let us know if you have any
suggestions or spotted a bug. The preferred method of contribution is
through a GitHub pull request. Feel also free to contact us by creating
[an issue](https://github.com/nowosad/bespatial/issues).
