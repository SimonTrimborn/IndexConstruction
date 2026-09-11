# IndexConstruction: Index Construction for Time Series Data

`IndexConstruction` is an R package for constructing and maintaining market indices from time-series data. The package implements an index construction methodology that allows the number of index constituents to adjust flexibly to the underlying market structure.

The methodology is particularly useful for markets in which the number and relative importance of assets change over time. In addition to the flexible index construction approach, the package provides functionality for constructing market-capitalization-weighted and volume-weighted indices with a fixed number of constituents.

The main function of the package is `indexComp()`, which performs the complete index construction and returns the resulting index for further analysis. The package also provides the functions `indexMemberSelection()`, `indexMembersUpdate()`, and `indexUpdate()`. These functions allow the individual steps of the index construction procedure to be carried out separately and can be used to continuously update an existing index.

The methodology implemented in this package was introduced in:

**Trimborn, S. and Härdle, W. K. (2018). _CRIX an Index for cryptocurrencies_. Journal of Empirical Finance, 49, 107–122. doi:10.1016/j.jempfin.2018.08.004.**

## Installation

The package can be installed directly from GitHub. To do so, you first need the `devtools` package.

If `devtools` is not installed yet, run:

```r
install.packages("devtools")
```

Then load `devtools`:

```r
library(devtools)
```

You can now install the latest version of `IndexConstruction` from GitHub:

```r
install_github("SimonTrimborn/IndexConstruction")
```

After installation, load the package with:

```r
library(IndexConstruction)
```

The package is also available from CRAN and can be installed using:

```r
install.packages("IndexConstruction")
```

## Main functionality

The main function for constructing an index is:

```r
indexComp(...)
```

It combines the different steps required for index construction, including the selection and updating of index constituents.

For applications in which the index needs to be updated continuously, the individual components can also be used separately:

```r
indexMemberSelection(...)
indexMembersUpdate(...)
indexUpdate(...)
```

This makes the package suitable both for empirical analysis and for applications in which an index is regularly recalculated and published.

## Reference

When using `IndexConstruction` in academic work, please cite:

**Trimborn, S. and Härdle, W. K. (2018).  
CRIX an Index for cryptocurrencies.  
Journal of Empirical Finance, 49, 107–122.  
doi:10.1016/j.jempfin.2018.08.004.**