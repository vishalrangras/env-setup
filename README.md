# Environment Configuration

This repository contains the details and configuration file to install all the Deep Learning related dependencies of Python on Anaconda Environment. At present, the bare minimum libraries are provided in the configuration file `environment.yml`. As we will proceed further in the learning curve and as we will explore more libraries, we will keep them adding to the configuration file. Feel free to fork this repository and send a pull request whenever you would like to add suitable dependencies to the config file or would like to suggest additional environment setup related approaches.

As per the Anaconda [docs](http://conda.pydata.org/docs):

> Conda is an open source package management system and environment management system 
for installing multiple versions of software packages and their dependencies and 
switching easily between them. It works on Linux, OS X and Windows, and was created 
for Python programs but can package and distribute any software.

## Overview
We need to follow 3 simple steps to get our environment up and running:

1. Install [`Anaconda`](https://www.continuum.io/downloads) on your computer from direct link or \\\\192.168.102.226 location.
2. Follow the environment setup instructions below to create a new `conda` [environment](http://conda.pydata.org/docs/using/envs.html)
3. Each time you wish to work, activate your `conda` environment. Easy peasy!

## Installation

**Download** the version of `Anaconda` that matches your system from https://www.continuum.io/downloads
Following versions are available on the site:

|        | Linux | Mac | Windows | 
|--------|-------|-----|---------|
| 64-bit | [64-bit (bash installer)][lin64] | [64-bit (bash installer)][mac64] | [64-bit (exe installer)][win64]
| 32-bit | [32-bit (bash installer)][lin32] |  | [32-bit (exe installer)][win32]

## Create Environment

**Pre-requisite:** You must have git installed in your system and added to the Path variable.

**Setup:** Create one directory in your local system to clone this repository and open that directory in Ananconda prompt. Running the following commands will create a new `conda` environment that is provisioned with all libraries you need for deep-learning.

```sh
git clone https://github.com/vishalsrangras/env-setup.git
cd env-setup
conda env create -f environment.yml
```

**Verify** that the `deep-learning-env` environment was created in your environments:

```sh
conda info --envs
```

You can alternatively also use:
```sh
conda envs list
```

**Cleanup** downloaded libraries (remove tarballs, zip files, etc) after the successful setup of environment:

```sh
conda clean -tp
```

### Uninstalling 

To uninstall the environment from your machine, use the following command:

```sh
conda env remove -n deep-learning-env
```

---

## Using Anaconda

Once the Anaconda environment is created, in order to use it, you will need to activate the environment. This must be done **each** time you begin a new working session i.e. open a new terminal window. 

**Activate** the `deep-learning-env` environment:

### OS X and Linux
```sh
$ source activate deep-learning-env
```
### Windows
```sh
$ activate deep-learning-env
```

That's it. Now all of the `deep-learning-env` libraries are available at your disposal.

To exit the environment when you have completed your work session, simply close the terminal window.
