# data-exploration
Preliminary data exploration notebooks


# Running Jupyter notebooks from here
(Thor): I've created a Pipfile and a shell script that will allow you to easily start 
a Jupyter notebook that has all the right packages. You might not need it if you 
already have a jupyter server up and running, say through conda. I've also aimed these
instructions at \*nix (including Mac), so if you use Windoze, well...

The notebook will by default install commonly used data science packages such as
`numpy`, `scipy`, `pandas`, `tensorflow`, `xgboost`, `matplotlib`, `plotly`, 
`bokeh`, `statsmodels`, `seaborn`, `pydot`, `scikit-learn`, `eli5`, `tpot`,
`dask`,  `nltk`, `spacy`, `scrapy`, `db-sqlite3`, `pymongo`, `requests`, `mysql-python` 

It installs to a virtualenv just for this notebook server, so you won't
mess up your system python.

## Prerequisites
I'm assuming you already have the following installed:
* Python 3.7 (if you haven't already got python3.7 installed, try installing pyenv to allow multiple concurrent 
versions of python)
* pip (https://pip.pypa.io/en/stable/installing/)
* pipenv (https://pipenv.readthedocs.io/en/latest/)

## Installing
```
pipenv install
```
Will install all the packages in the Pipfile.
You can run it again any time and it will install install any new packages people have added
(and won't need to reinstall everything you've already done)


## Adding new packages
If you want to add some new packages, say `graphviz` in this example, just do this from your command line
(in the directory where you cloned):

```
pipenv install graphviz
```

It will add it to the Pipfile, so other people know what packages are in use and can
just `pipenv install` or `pipenv sync` to get the required packages to run your notebook. Remember to 
(git) commit your Pipfile if you modify it!


## Running
After you've done that first installation, it's really quick to get notebooks up and running:

```
pipenv run jupyter notebook
```

and BOOM! You're good to go.

I'm also forgetful, so I just added a `run-notebook.sh` script to do the above step.

It should open up a browser to your notebook server, but it's running on http://localhost:8888 anyway.





