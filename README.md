# r-binder-template

A template repository for binderising one off R notebooks for workshops and training.

This repository is intended as a compact template for deploying one off
notebooks and training materials for customised workshops. 

# Usage

1. Click the "Use this template" in the GitHub web UI to create a new repository
with these skeleton elements for binderisation.
2. The default R version is 4.2.2. If you want to use a later version, you can choose the R version and put it in runtime.txt in the format: `r-a.b.c-YYYY-MM-DD`
where a.b.c is the R version number and YYYY-MM-DD is a snapshot date for packages.
3. Specify R dependencies in install.R, using standard R installation syntax: `install.packages('dplyr')`
4. Specify systems dependencies in apt.txt, with one line per package and the required package name
5. Whack your notebook (either ipynb or Rmd) and associated small data files in the repo. 
	- For a single jupyter notebook this might just be at the root of the repo
	- You might want to put data files in a data subfolder
	- If you want to share a few notebooks in the same repo, it might be better to 
	  place in a notebooks subfolder 
6. Customise the readme and description as appropriate.
7. Adapt the link to Binder so that Binder can fire up ypur notebook. For the present tutorial, the link looks as follows: https://mybinder.org/v2/gh/mschw81/main?labpath=notebooks%2Facqvainter_cb.ipynb
8.
9. Setup the binder link on the [ATAP Binder Instance](https://binderhub.atap-binder.cloud.edu.au/) 
or [My Binder](https://mybinder.org/) (Broadly accessible, but lower memory/CPU limits). You will
point binder to the repository you have created from this template, probably using the `main` branch, 
and providing the name of the notebook you want to be launched by default (if desired).
10. Place the generated binder link (ideally with the Binder icon) in the readme.

