<!--TOC using https://github.com/ekalinin/github-markdown-toc-->
<!--ts-->
   * [Pandas for Everyone](#pandas-for-everyone)
   * [Setup](#setup)
      * [Install seaborn for plotting](#install-seaborn-for-plotting)
      * [Install all the packages used in the book](#install-all-the-packages-used-in-the-book)
         * [(Optional) Create a Virtual Environment](#optional-create-a-virtual-environment)
         * [Install the packages](#install-the-packages)
   * [Teaching Slides](#teaching-slides)
      * [No Powerpoint (.ppt/.odp)](#no-powerpoint-pptodp)
   * [Data](#data)
   * [Links to teaching sessions](#links-to-teaching-sessions)

<!-- Added by: dchen, at: 2018-04-05T23:01-04:00 -->

<!--te-->

# Pandas for Everyone
Repository to accompany "Pandas for Everyone"

# Setup

The easiest way to get everything you need to the tutorial is to install `anaconda`

You can download and install it here: https://www.continuum.io/downloads

To download just the data, see the [Data](https://github.com/chendaniely/pandas_for_everyone#data) section below.
Otherwise you can choose to clone this repository, or click the "Clone or Download" link above and clikcing [Download Zip](https://github.com/chendaniely/pandas_for_everyone/archive/master.zip)

## Install seaborn for plotting

`conda install seaborn`

## Install all the packages used in the book
There is an error in the preface of the book for installing packages.
I am leaving this section here in the README to have an updated list of packages and installation instructions

### (Optional) Create a Virtual Environment

You can choose to create a virtual envirionment for the packages used in the book,
so it doesn't clash with other packages you plan to use later on.

```bash
# create a virtual environment named "book" using python 3.6
conda create -n book python=3.6

# activate the environment
# so all installed packages will go in there and not mess up your base python environment
source activate book
```

### Install the packages

Whether you decited to create a virtual environment or not, you can install the packages with the below commands.
If you did use virtual environments, remember to `source activate book` before you follow along with the book
so the packages you installed can be loaded.

```bash
conda install pandas xlwt openpyxl seaborn numpy ipython jupyter statsmodels scikit-learn regex wget odo numba
conda install -c conda-forge pweave # you don't really need this package, it was used to build and create the book
conda install -c conda-forge feather-format
pip install lifelines pandas-datareader
```

# Teaching Slides

For those instructors who are using the teaching slide deck version of the book.
Each chapter is split into it's own slide deck.
There are multiple versions for each chapter.

1. Jupyter notebook (ipynb)
2. PDF
3. HTML

The slides are created using
[Damian Avila's](http://www.damian.oquanta.info/)
[RISE](https://damianavila.github.io/RISE/index.html)
Jupyter/IPython Slideshow Extension.
Thus, you can choose to install the RISE extension and live render and display the Jupyter notebooks (ipynb).
Since each chapter is a Jupyter notebook at heart, the conversions to PDF and HTML are performed using

```bash
jupyter nbconvert --to slides your_talk.ipynb --post serve
```

More about useage ange converting to the PDF can be found on the RISE documentation page on
[useage](https://damianavila.github.io/RISE/usage.html).

## No Powerpoint (.ppt/.odp)

RISE's back end uses reveal.js.
Unfortunately there is [no way to go from a reveal.js presentation to powerpoint](https://github.com/hakimel/reveal.js/issues/1702).
Having said that,
if there's a way we can jerry-rig something together using the the given capabilties of RISE and reveal.js please let me know.

# Data

You can choose to *just* download the datasets by using [Minhas Kamal's](https://minhaskamal.github.io/#/home) [DownGit](https://minhaskamal.github.io/DownGit/#/home) by clicking the link [here](https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/chendaniely/pandas_for_everyone/tree/master/data)

Ongoing list of data references:

1. Gapminder: https://github.com/jennybc/gapminder/raw/master/inst/gapminder.tsv
2. Survey: Comes from the [Software-Carpentry](http://software-carpentry.org/) SQL [lesson](http://swcarpentry.github.io/sql-novice-survey)
3. Ebola: www.github.com/cmrivers/ebola

# Links to teaching sessions

- https://github.com/chendaniely/2017-12-04-pandas_live
- https://github.com/chendaniely/2017-10-26-python_crash_course
- https://github.com/chendaniely/scipy-2017-tutorial-pandas
    - https://github.com/chendaniely/scipy_2017_notes
    - https://www.youtube.com/watch?v=oGzU688xCUs
- https://github.com/chendaniely/2016-pydata-carolinas-pandas
