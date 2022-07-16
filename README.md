# Depository

A CRAN-like package repository for previously released R packages originating from this organization.

## Usage

Set the repository options in R to point to this repository to point to the `2022_06_09` release, then run the following in an R session:

```R
options(
    repos = c(
        insightsengineering = "https://insightsengineering.github.io/depository/2022_06_09",
        CRAN = "https://cloud.r-project.org/"
    )
)
```

Next, assuming you want to install the `teal` package, simply run this in the R session:

```R
install.packages("teal")
```

## How was this repository created?

Pre-built versions of the releases were added to the corresponding release directory, and the following command was run in R to create a repository.

```R
tools::write_PACKAGES()
```

## How does this work, exactly?

This repository uses Github Pages to serve packages.
