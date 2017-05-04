# Environment Configuration

This repository contains the details and configuration file to install all the Machine Learning / Deep Learning related dependencies of Python on Anaconda Environment.

Per the Anaconda [docs](http://conda.pydata.org/docs):

> Conda is an open source package management system and environment management system 
for installing multiple versions of software packages and their dependencies and 
switching easily between them. It works on Linux, OS X and Windows, and was created 
for Python programs but can package and distribute any software.

## Overview
Using Anaconda consists of the following:

1. Install [`Anaconda`](https://www.continuum.io/downloads) on your computer from direct link or \\192.168.102.226 location.
2. Follow the environment setup instructions below to create a new `conda` [environment](http://conda.pydata.org/docs/using/envs.html)
3. Each time you wish to work, activate your `conda` environment

## Installation

**Download** the version of `Anaconda` that matches your system from https://www.continuum.io/downloads

|        | Linux | Mac | Windows | 
|--------|-------|-----|---------|
| 64-bit | [64-bit (bash installer)][lin64] | [64-bit (bash installer)][mac64] | [64-bit (exe installer)][win64]
| 32-bit | [32-bit (bash installer)][lin32] |  | [32-bit (exe installer)][win32]

## Create Environment

**Setup** your `deep-learning-env` environment. Open the Anaconda terminal. Running the following commands will create a new `conda` environment that is provisioned with all libraries you need for deep-learning.

```sh
git clone https://github.com/vishalsrangras/env-setup.git
cd env-setup
conda env create -f environment.yml
```

**Verify** that the `deep-learning-env` environment was created in your environments:

```sh
conda info --envs
```

**Cleanup** downloaded libraries (remove tarballs, zip files, etc):

```sh
conda clean -tp
```

### Uninstalling 

To uninstall the environment:

```sh
conda env remove -n deep-learning-env
```

---

## Using Anaconda

Now that you have created an environment, in order to use it, you will need to activate the environment. This must be done **each** time you begin a new working session i.e. open a new terminal window. 

**Activate** the `deep-learning-env` environment:

### OS X and Linux
```sh
$ source activate deep-learning-env
```
### Windows
```sh
$ activate deep-learning-env
```

That's it. Now all of the `deep-learning-env` libraries are available.

To exit the environment when you have completed your work session, simply close the terminal window.
