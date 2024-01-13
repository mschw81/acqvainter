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
7. Adapt the link to Binder so that Binder can fire up your notebook. For the present tutorial, the link looks as follows: https://mybinder.org/v2/gh/mschw81/acqvainter/main?labpath=notebooks%2Facqvainter_cb.ipynb
   There are three sequences you need to adapt:
   + the user name (*mschw81* is my GitHub username) 
   + the repo name (*acqvainter* is the repo name)
   + the notebook name (*acqvainter_cb.ipynb* is the notebook name).
As an alterntive, you can also upload your Jupyter notebook into Google Colab and share it with others. The issue is that Google Colab will kick you out if computations (including package installations) take too long and you have rather limited computing power. 

Be aware that the first time you start your interactive notebook, the set up will take very long because a Docker image (a virtual machine) with all required software applications and packages will be created from your GitHub repository. This can take up to an hour if your notebook is very complex and has many dependencies. Simpler notebooks fire up much faster but will take at least 10 minutes to start when you first fire them up.

