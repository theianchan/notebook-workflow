## New project workflow
1. `mkdir $project_name; cd $project_name`
2. (Requires `virtualenvwrapper` in global) `mkvirtualenv $project_name`
3. (Requires `ipykernel` in the project environment `pip install ipykernel`) `python -m ipykernel install --user --name $project_name --display-name "Python ($project_name)"`
4. `jupyter notebook` should have a new kernel option for "Python ($project_name)"

## Git workflow
1. `pip freeze > requirements.txt`
2. No need to add any `/venv/` folders to `.gitignore` because thanks to `virtualenvwrapper` this isn't stored in the project folder.
3. `git add`, `git commit` etc

## Running project from a different machine (probably Paperspace)
1. `git clone $project_name; cd $project_name`
2. (Requires `virtualenvwrapper`) `mkvirtualenv $project_name`
3. `pip install -r requirements.txt`
4. (Requires `ipykernel` in the project environment) `python -m ipykernel install --user --name $project_name --display-name "Python ($project_name)"`
5. `jupyter notebook` should have a new kernel option for "Python ($project_name)"

## Venv use
1. `workon $project_name`
2. `deactivate`

## Reference
Kernel install locations (`rm` these to uninstall):

1. `/users/$user/library/jupyter/kernels`
2. `/usr/local/share/jupyter/kernels`

Or check `jupyter --paths`.

## Helpful
1. [Python virtualenv primer](https://realpython.com/python-virtual-environments-a-primer/)
2. [Kernels for different Python versions/different environments](http://ipython.readthedocs.io/en/stable/install/kernel_install.html)

