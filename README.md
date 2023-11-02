# Assignment 2

This archive contains instructions/information if you wish to develop and test you code locally.

The `src/` folder contains the boilerplate files (similarly to the CodeGrade editor). You can copy paste your code to the respective CodeGrade task once you are done.


## Quick setup
> **Note**
> This setup will use the default python installed on your machine. It is convenient in order to test the correctness of your program but might yield wrong execution times as on CodeGrade we use [PyPy](https://www.pypy.org/).

```bash
# Install the required packages to python
python -m pip install -U -r requirements.txt

# Run the tests for a specific task where X in [1, 3]
pytest test_assignment_2_shared -m task_X

# Run the tests for all tasks 
pytest test_assignment_2_shared
```

## Pyenv setup
If you wish to test locally in a similar environment as the `CodeGrade` instances, and, are familiar with [pyenv](https://github.com/pyenv/pyenv), you can use the following setup. If you are more familiar with `conda` you can search on the web on how to install PyPy there.

> **Warning**
> Keep in mind that while PyPy will be used if you follow the setup, execution times might still be affected by the power of your machine. **You code is graded on whether the tests pass on CodeGrade and not your own machines**


```bash
# Install pypy
pyenv install pypy3.8-7.3.9
# Set pypy as default python
pyenv global pypy3.8-7.3.9
# If you run `python -V` you should see `[PyPy 7.3.9....]`

# Install the required packages
python -m pip install -U -r requirements.txt

# Run the tests for a specific task where X in [1, 3]
pytest test_assignment_2_shared -m task_X

# Run the tests for all tasks 
python -m pytest test_assignment_2_shared  # (`python -m` can be omitted)

# Restore python version when you are done
pyenv global system
```