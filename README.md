# guide-build-python-environment

## `conda`
- This is a guide a setup a python environment using `conda` for Windows
- A description of `conda` can be found on https://docs.conda.io/projects/conda/en/latest/, a brief description copied from that page is pasted below

*Package, dependency and environment management for any language---Python, R, Ruby, Lua, Scala, Java, JavaScript, C/ C++, FORTRAN*

*Conda is an open-source package management system and environment management system that runs on Windows, macOS, and Linux. Conda quickly installs, runs, and updates packages and their dependencies. Conda easily creates, saves, loads, and switches between environments on your local computer. It was created for Python programs but it can package and distribute software for any language.*

- There are a few different terms; `conda`, Anaconda, Miniconda, `conda-forge`. More information on these can be found on https://docs.conda.io/projects/conda/en/latest/glossary.html.
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
