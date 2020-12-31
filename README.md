# guide-build-python-environment

## `conda`
- This is a guide a setup a python environment using `conda` for Windows
- A description of `conda` can be found on https://docs.conda.io/projects/conda/en/latest/, a brief description copied from that page is pasted below

*Package, dependency and environment management for any language---Python, R, Ruby, Lua, Scala, Java, JavaScript, C/ C++, FORTRAN*

*Conda is an open-source package management system and environment management system that runs on Windows, macOS, and Linux. Conda quickly installs, runs, and updates packages and their dependencies. Conda easily creates, saves, loads, and switches between environments on your local computer. It was created for Python programs but it can package and distribute software for any language.*

- There are a few different terms; `conda`, Anaconda, Miniconda, `conda-forge`. More information on these can be found on https://docs.conda.io/projects/conda/en/latest/glossary.html
- For us, we want to choose between Anaconda and Miniconda. The main difference is that Anaconda ships with a large number of data science python packages whereas Miniconda is a very basic and bare bones
    - Due to this there is a difference in size of the installation file, i.e. Anaconda is much bigger than Miniconda
    - Both installations will provide an instance of `conda` which is the command line interface tool for package management
- Once we have `conda` installed, we can do the following things:
    - Create multiple python environments independent of each other
    - Remove python environments
    - Install python packages and other dependencies using `conda`

### Installation

- We can use the following powershell script to install Miniconda, some minor changes will also allow the user to install Anaconda if that is preffered
- Please find the script at https://gist.github.com/joy-rosie/dabf8a5511d5e6bd334a605fb5bd2c5c
- Once this is done, open a `conda` prompt and run:

```
conda update conda
```

- `conda` will have a base environment `(base)` which can be seen in the prompt and this is itself an environment
- We can create more environments than just the `base` environment
    - The idea is to create different environments for different projects to keep the dependencies clean
    - This is not necessary if we are doing simple projects for learning and playing around but as soon as we would like to share projects or code, it will be useful to have an environment dedicated to that project

### Useful commands
- Create a new environment

```
conda create -n <name> python=3.8
```

- Create an environment using an available `environment.yml` file

```
conda env create -f <path to environment.yml>
```

- Activate an environment

```
conda activate <name>
```

- Deactivate the environment we are in

```
conda deactivate
```

- Remove an environment

```
conda env remove -n <name>
```

## `git`

- Another important part of the python setup is `git`, this is an open source software used for version control for text base files
- More information on `git` can be found on https://git-scm.com/about
- Version control is important when collaborating and also for "saving" different parts of the development cycle so we can go back to the right place
- `git` is also the underlying software used within GitHub, GitLab, BitBucket
- With `git` we can download any `git` repository onto our computer with a single line of code
- We can install `git` from https://git-scm.com/downloads and recommend using default settings along the way
