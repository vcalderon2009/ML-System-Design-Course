[![alt Course Link][CourseWebsiteIMG]][course_website_link]
[![alt Syllabus Link][SyllabusIMG]][course_syllabus_link]
![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/vcalderon2009/ML-System-Design-Course/code-linting.yml)

# ML System Design

This repository covers the tasks from the "[ML System Design](https://maven.com/boring-bot/ml-system-design/1/home)" course.

## Table of Contents

- [Rules and guidelines](#rules-and-guidelines)
- [The Structure of the Project](#the-structure-of-the-project)
- [Setup for local code development](#setup-for-local-code-development)
  - [Makefile](#makefile)
  - [Initializing the repository](#initializing-the-repository)
  - [Install Python environment](#install-python-environment)
  - [Linting the code and checking for any errors](#linting-the-code-and-checking-for-any-errors)
  - [Cleaning any leftover Python artifacts](#cleaning-any-leftover-python-artifacts)


## Rules and guidelines

In order to get the best out of the template:

* Don't remove any lines from the `.gitignore` file we provide
* Don't commit data to your repository
* Don't add any secrets or passwords to the repository!

## The Structure of the Project

The components are as follows:

* __Makefile__ : File containing all of the functions of the project that
one can run the inference script (and possibly training script), build the
Docker image, and more.

## Setup for local code development

There are some steps that need to be done prior to being able to
properly run and develop the code in this repository.

The followign is a list of steps that have to happen prior to starting to
work / test the pipelines of this repository:

### Makefile

The project comes with a `Makefile` (**not supported in Windows!**)
that can be used for executing commands that will make the interaction
with this project much smoother.

One can see all of the available options by:

```bash
    $: make

    Available rules:

    add-licenses              Add licenses to Python files
    clean                     Removes artifacts from the build stage, and other common Python artifacts.
    clean-build               Remove build artifacts
    clean-model-files         Remove files related to pre-trained models
    clean-pyc                 Removes Python file artifacts
    clean-secrets             Removes secret artifacts - Serverless
    clean-test                Remove test and coverage artifacts
    create-environment        Creates the Python environment
    create-envrc              Set up the envrc file for the project.
    delete-environment        Deletes the Python environment
    delete-envrc              Delete the local envrc file of the project
    destroy                   Remove ALL of the artifacts + Python environments
    init                      Initialize the repository for code development
    lint                      Run the 'pre-commit' linting step manually
    pip-upgrade               Upgrade the version of the 'pip' package
    pre-commit-install        Installing the pre-commit Git hook
    pre-commit-uninstall      Uninstall the pre-commit Git hook
    requirements              Install Python dependencies into the Python environment
    show-params               Show the set of input parameters
    sort-requirements         Sort the project packages requirements file
    test                      Run all Python unit tests with verbose output and logs
```

> **NOTE**: If you're using `Windows`, you may have to copy and modify to some
> extents the commands that are part of the `Makefile` for some tasks.

### Initializing the repository

The `Makefile` comes with a predefined set of functions that makes it easy
to set up the project repository.

To initialize the repository, one could simply run:

```bash
# Initializing repository
make init
```

This will perform the following tasks:
- Remove any unnecessary Python artifacts.
- Create the `.envrc` file of the repository.
- Delete any prior Python environment.
- Create new and empty Python environment for the project.
- Install the necessary Python packages into the environment.
- Install [pre-commit](https://pre-commit.com/) for linting purposes.

### Install Python environment

The `Makefile` comes with a pre-built set of functions to install the
necessary Python environments.

> **NOTE**: If this is the first time using Anaconda on your computer
> (e.g. after starting a new Pod), you may have to **initialize** `conda`:

```bash
# If you're running bash
conda init bash

# If you're running zsh
conda init zsh
```
and then restart the shell and create the new environment!

If the command `make init` worked well, you should be able to use the
Python environment without any issues.

Is using Anaconda:

```bash
conda activate ML_System_Design_Course
```


### Linting the code and checking for any errors

The repository comes with tools to validate the scripts of the repository and
look for any issues in terms of code linting, missing variables, unused
imported packages, etc.

To use this for **the very first time**, you must first install the
`git` hooks from [`pre-commit`](https://pre-commit.com/):

```bash
# Install the necessary hooks to your Python environment
make pre-commit-install
```

In order to continuously check for errors as one is developing the code,
one can simply run:

```bash
make lint
```

This command will run `pre-commit` and check for any issues in the current
version of the code.

### Cleaning any leftover Python artifacts

As one is developing the code, one can remove artifacts from the various
stages of code development (e.g. *build* stage, compiling stage, etc.).

In order to remove these files and directories, one can run:

```bash
make clean
```

This will call different functions from the Makefile and remove these
artifacts from the repository.


<!-- Links -->

[course_syllabus_link]: https://night-rhodium-552.notion.site/MAVEN-Machine-Learning-System-Design-with-Large-Language-Models-2da50f163ccd4eb0879f41e357478f01

[SyllabusIMG]: https://img.shields.io/badge/Course-Syllabus-orange (syllabusimg)

[course_website_link]: https://maven.com/boring-bot/ml-system-design

[CourseWebsiteIMG]: https://img.shields.io/badge/Course-Website-blue (courseimg)
