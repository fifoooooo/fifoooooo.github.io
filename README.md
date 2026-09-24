## Introduction

My personal website, built with Quarto. It includes blog posts with data analysis in both Python and R.

## How I Built the site

Firstly, I went to my folder and made sure everything I had for the creation of my website was intact

$ ls
```_quarto.yml                index.qmd
about.qmd                  Milestone 2 submission.pdf
blog.qmd                   posts
docs                       README.md
images                     styles.css 
```

Install these first: 
```
$ quarto --version
1.10.18
$ uv --version
uv 0.12.5 (210d1f678 2026-08-14 aarch64-apple-darwin)
$ R --version
R version 4.6.1 (2026-06-24) -- "Happy Hop"
```

All commands below were run in my terminal from the repository root unless stated otherwise.

1. Clone the repository and move into it:

```bash
   git clone git@github.com:fifoooooo/fifoooooo.github.io.git
   cd fifoooooo.github.io
```

2. Install the Python environment (Python 3.14, pandas, numpy, jupyter)
   from `uv.lock`:

```bash
   uv sync
```

3. Install the R packages (tidyverse, testthat, and dependencies) from
   `renv.lock`. The first run bootstraps renv automatically:

```bash
   Rscript -e 'renv::restore()'
```

   Type `y` if asked to proceed. (Alternatively, open R in this folder
   and run `renv::restore()` in the R console.)

4. Render the site:

```bash
   uv run quarto render
```

## Viewing the site

The built site is written to the `docs/` folder. To view it locally,
open `docs/index.html` in a web browser, or run:

```bash
uv run quarto preview
```

and open the address it prints (e.g. `http://localhost:XXXX`).

## Data

Both datasets are included in the repository, so the build does not
need the network to fetch data. (Steps 2 and 3 do need the network to
download packages.)

- `posts/housing-finance/Housing_finance.csv`: Housing Finance Agency
  Portfolio, from [Data.gov](https://catalog.data.gov/dataset/housing-finance-agency-portfolio).
- `posts/can_lang/can_lang.csv`: 2016 Canadian Census language data,
  from the [canlang package](https://github.com/ttimbers/canlang) by
  Tiffany Timbers, via the
  [UBC-DSCI textbook repository](https://github.com/UBC-DSCI/introduction-to-datascience/blob/main/data/can_lang.csv).



Personl Reference for me:
For notes on how this project was originally set up, see [_setup-log.md](_setup-log.md).



