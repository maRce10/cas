sketchy
================

<!-- README.md is generated from README.Rmd. Please edit that file -->

<!-- [![CRAN\_Status\_Badge](http://www.r-pkg.org/badges/version/sketchy)](https://cran.r-project.org/package=sketchy) -->

<!-- [![CRAN RStudio mirror downloads](http://cranlogs.r-pkg.org/badges/sketchy)](http://www.r-pkg.org/pkg/sketchy) -->

<!-- [![Total downloads](https://cranlogs.r-pkg.org/badges/grand-total/sketchy?color=blue)](https://r-pkg.org/pkg/sketchy) -->

[![lifecycle](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://www.tidyverse.org/lifecycle/#experimental)

The package is intended to facilitate the use of research compendiums
for data analysis in the R environment. Standard research compendiums
provide a easily recognizable means for organizing digital materials,
allowing other researchers to inspect, reproduce, and build upon that
research.

<!-- Unlike other packages for setting up research compendiums, `sketchy` has very simple functionality. Hence, users can focus on the research project itself rather than on learning how to use a new R package. -->

Unlike other R packages for creating research compendiums
(e.g. [vertical](https://github.com/CrumpLab/vertical),
[rrtools](https://github.com/benmarwick/rrtools)), `sketchy` isn’t
wedded to a particular folder structure. Currently the package provides
13 alternative structures (see object `compendiums`) and allows users to
modify or input their own structures.

To install the latest developmental version from
[github](http://github.com/) you will need the R package
[devtools](https://cran.r-project.org/package=devtools):

``` r

# From github
devtools::install_github("maRce10/sketchy")

# load package
library(sketchy)
```

## Default compendium skeletons

Compendiums can be set up with the function `make_compendium()`. The
function creates the folder/subfolder structure and prints a diagram of
the skeleton in the console:

### Basic compendium

``` r

path = tempdir()

make_compendium(name = "proyect_x", path = path, format = compendiums$basic$skeleton)
```

<img src="./inst/compendium_1.png" width="55%" />

 

(*in these examples the compendiums are created in a temporary
directory, change ‘path’ to create it in a different directory*)

### Boettiger

``` r

make_compendium(name = "proyect_y", path = path, format = compendiums$wilson$skeleton)
```

<img src="./inst/compendium_2.png" width="55%" />

 

We can also add comments to the folders to explain what kind of files
they are supposed to contain:

``` r

make_compendium(name = "proyect_z", path = path, format = compendiums$large_compendium$skeleton, 
    comments = compendiums$large_compendium$comments)
```

<img src="./inst/compendium_3.png" width="65%" />

 

When creating a compendium that includes a “manuscript” folder the
package adds a “manuscript\_template.Rmd” file for facilitating paper
writing within the compendium itself.

-----

Please cite [sketchy](https://marce10.github.io/sketchy/) as follows:

Araya-Salas, M., Willink, B., Arriaga, A. (2020), *sketchy: research
compendiums for data analysis in R*. R package version 1.0.0.

# References

1.  Marwick, B., Boettiger, C., & Mullen, L. (2018). *Packaging Data
    Analytical Work Reproducibly Using R (and Friends)*. American
    Statistician, 72(1), 80–88.

2.  Alston, J., & Rick, J. (2020). *A Beginner’s Guide to Conducting
    Reproducible Research*.
