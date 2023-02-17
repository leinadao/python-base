[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit)

# Python Base
A base python setup

## Set up in a repo:
```
  git remote add python-base git@github.com:leinadao/python-base.git
  git fetch python-base
  git rebase python-base/main # Resolve any conflicts.
  git push # possibly need --force
```
Update latest base changes in a repo:
```
  git fetch python-base
  git rebase python-base/main # Resolve any conflicts.
  git push # possibly need --force
```

=======

## Setup:
```
brew install poetry
```
Storing the virtual environment in the source directory allows VSCode to find and activate it, which means that e.g. flake8 plugins are found and run.

At the moment poetry venv location can't be set in pyproject.toml, only in poetry.toml which should be local and not source-controlled.

So instead a manual config change is required:
```
poetry config virtualenvs.in-project true
```
Any existing venvs can be removed:
```
poetry env list
poetry env remove ...
```
Then install at the expected location:
```
poetry install
```


# TODO: Use pre-commit to ensure latest base repo has been rebased in?
