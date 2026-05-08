# tinnlab drat archive

Pre-built binary R packages from the [Tin Nguyen Lab](https://github.com/tinnlab).

This is a [drat](https://github.com/eddelbuettel/drat) archive served via GitHub Pages at
<https://tinnlab.github.io/drat/>. It hosts compiled binaries only — source repositories are private.

## Available packages

| Package | Description |
|---|---|
| **PRESS** | Perturbation-Resampled Enrichment with Semantic Smoothing — gene set enrichment analysis with a C++ core |

## Install

### macOS (Intel or Apple Silicon) and Windows

```r
install.packages("PRESS",
                 repos = "https://tinnlab.github.io/drat",
                 type  = "binary")
library(PRESS)
?PRESS
```

R will pick the right binary for your platform and R version automatically.

### Linux (x86_64)

R does not auto-install binary packages on Linux. Install directly from URL:

```r
# Pick the binary that matches your R version (4.2 / 4.3 / 4.4 / 4.5 / 4.6).
# Replace <R-VERSION> below with your major.minor (e.g. 4.6).
url <- sprintf(
  "https://tinnlab.github.io/drat/bin/linux/contrib/%s/PRESS_<VERSION>_R_x86_64-pc-linux-gnu.tar.gz",
  "<R-VERSION>")
download.file(url, "/tmp/PRESS.tar.gz")
install.packages("/tmp/PRESS.tar.gz", repos = NULL, type = "binary")
```

If you don't know your R version: `getRversion()`.

## Supported platforms

Each release builds for:

| OS | Architecture | R versions |
|---|---|---|
| Linux | x86_64 | 4.2, 4.3, 4.4, 4.5, 4.6 |
| macOS Apple Silicon | arm64 | 4.3, 4.4, 4.5, 4.6 |
| Windows | x86_64 | 4.2, 4.3, 4.4, 4.5, 4.6 |

> Note: macOS Intel (x86_64) binaries are not provided. Intel-Mac users will need to build from source — contact the author for the source tarball.

## Contact

Phi Bya — phi@wayne.edu
