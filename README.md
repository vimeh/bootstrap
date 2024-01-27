#!/bin/sh

# Bootstrap a python virtualevn with poetry

#### This script is meant to be run from the root of the repo

#### run this script from the root of the repo

#### you'll need to have brew installed. this is easier if you have a darwin machine

```bash
# uncomment the next line if you're like me and think fish is a better shell.
# brew install fish && fish && set -U fish_user_paths /usr/local/bin $fish_user_paths
brew install python@3.11
python3.11 -m pip install pipx
pipx install poetry --force
rm pyproject.toml
poetry init
# go thru the poetry wizard (!)
poetry env use 3.11
poetry add numpy
poetry install
poetry shell
code .
```
