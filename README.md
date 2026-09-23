# Steps to follow: 
Firstly, I went to my folder and made sure everything I had for the creation of my website was intact
$ cd /Users/eniolaoladimeji/UBC\ MDS/fifoooooo.github.io\ \(my\ website\) 
$ ls
_quarto.yml                index.qmd
about.qmd                  Milestone 2 submission.pdf
blog.qmd                   posts
docs                       README.md
images                     styles.css

# Ran positron, verified Python & Quarto version
$ positron .
$ python --version
$ quarto --version
$ python3 -m pip install jupyter
$ quarto check jupyter
$ uv init --bare --name my-website
$ uv sync
$ source .venv/bin/activate
$ uv add pandas
$ uv add numpy
$ grep venv .gitignore
$ echo ".venv/" >> .gitignore

$ git status
$ git add pyproject.toml uv.lock .gitignore
$git push

$ mkdir -p posts/housing-finance
posts/housing-finance

$ mv Housing_finance.csv posts/housing-finance/
Housing_finance.csv -> posts/housing-finance/Housing_finance.csv

$ mkdir -p posts/can_lang
posts/can_lang

$ mv can_lang.csv posts/can_lang
can_lang.csv -> posts/can_lang/can_lang.csv

$ uv python pin 3.14
Pinned `.python-version` to `3.14`
$ uv add jupyter ipykernel
$ uv run quarto render

# initializing R 
$ renv::init()
$ git add renv.lock
$ git commit -m"Setup tidyverse and testthat for R"
$ uv run quarto render
$ git push

In R console 
> install.packages("yaml")
> install.packages("tidyverse")
> install.packages("testthat")
> renv::snapshot()

# Creating Index.qmd in each file
$ ls *posts
$ touch posts/can_lang/index.qmd
$ touch posts/housing-finance/index.qmd

# making sure python was running in the right folder
$ import os
$ os.chdir("posts/housing-finance")
$ quarto preview

# Positron Terminal 
Python 3.14.7 (uv: my-website) started.
Python 3.14.7 (main, Aug 14 2026, 15:24:10) [Clang 22.1.3 ]
>>> import pandas as pd 


