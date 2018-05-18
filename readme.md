# Notebook Workflow

## New Project Workflow
1. `mkdir $project_name && cd $project_name`
2. (Requires virtualenvwrapper) `mkvirtualenv $project_name`
3. (Requires ipykernel in the project environment) `python -m ipykernel install --user --name $project_name --display-name "Python ($project_name)"`
4. `jupyter notebook` should have a new kernel option for "Python ($project_name)"

Next: what to git

## Reference
Kernel install locations:

1. `/users/$user/library/jupyter/kernels`
2. `/usr/local/share/jupyter/kernels`

Or check `jupyter --paths`.
