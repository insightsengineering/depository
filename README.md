# Depository

A CRAN-like package repository for previously released R packages originating from this organization.

**⚠️ Note**: This repository is a _temporary solution_ and a placeholder for packages that have not been published to CRAN yet. All of these packages will eventually be published to CRAN. Also, the _latest development_ versions of these packages are available on the [Pharmaverse r-universe repository](https://pharmaverse.r-universe.dev/ui).

## Usage

The following releases are available in this repository:

- [2022_06_09](./2022_06_09/src/contrib/)
- [2022_10_13](./2022_10_13/src/contrib/)

Set the repository options in R to point to a specific release in this repository:

```R
# Assuming you want to use the 2022_10_13 release
release_date <- "2022_10_13"
options(
    repos = c(
        insightsengineering = paste0(
            "https://insightsengineering.github.io/depository/",
            release_date
        ),
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
