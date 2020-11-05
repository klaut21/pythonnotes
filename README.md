# Python installation and configuration
Helpful links:

## Set python3 as default on mac
https://opensource.com/article/19/5/python-3-default-mac


### Using pyenv to install and select a specific python version
```bash
# install a specific python version
pyenv install 3.8.6
# set the current python version
pyenv global 3.8.6
```

## Setup a python virtual environment
https://opensource.com/article/19/6/python-virtual-environments-mac

You may already set up your long-term projects in a directory like ~/src. When you start working on a new project, go into this directory, add a subdirectory for the project, then use the power of Bash interpretation to name the virtual environment based on your directory name. For example, for a project named "pyfun":

```bash
$ mkdir -p ~/Documents/workspace/pyfun && cd ~/Documents/workspace/pyfun
$ mkvirtualenv $(basename $(pwd))
# we will see the environment initialize
(pyfun)$ workon
pyfun
test1
test2
(pyfun)$ deactivate
$
```

Whenever you want to work on this project, go back to that directory and reconnect to the virtual environment by entering:

```bash
$ cd ~/Documents/workspace/pyfun
(pyfun)$ workon .
```

Since initializing a virtual environment means taking a point-in-time copy of your Python version and the modules that are loaded, you will occasionally want to refresh the project's virtual environment, as dependencies can change dramatically. You can do this safely by deleting the virtual environment because the source code will remain unscathed:

```bash
$ cd ~/Documents/workspace/pyfun
$ rmvirtualenv $(basename $(pwd))
$ mkvirtualenv $(basename $(pwd))
```

## Getting started with JupyterLab
https://jupyter.org/install

If you use pip, you can install it with:
```bash
# install jupyterlab
$ pip install jupyterlab
# run jupyterlab
$ jupyter-lab
# Open http://localhost:8888/lab in browser
#  Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
```


