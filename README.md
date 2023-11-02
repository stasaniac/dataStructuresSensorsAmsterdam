# Fictional Project for Amsterdam sensors using arrays, dictionaries and heaps.

This archive contains instructions/information if you wish to develop and test the code locally.

The `src/` folder contains the boilerplate files. You can copy paste your code to the respective CodeGrade task once you are done.


## Quick setup
> **Note**
> This setup will use the default python installed on your machine. 

```bash
# Install the required packages to python
python -m pip install -U -r requirements.txt

# Run the tests for a specific task where X in [1, 3]
pytest test_assignment_2_shared -m task_X

# Run the tests for all tasks 
pytest test_assignment_2_shared
```

## Pyenv setup
If you wish to test locally in a similar environment as the instances, and, are familiar with [pyenv](https://github.com/pyenv/pyenv), you can use the following setup. If you are more familiar with `conda` you can search on the web on how to install PyPy there.

> **Warning**
> Keep in mind that while PyPy will be used if you follow the setup, execution times might still be affected by the power of your machine. 


```bash
# Install pypy
pyenv install pypy3.8-7.3.9
# Set pypy as default python
pyenv global pypy3.8-7.3.9
# If you run `python -V` you should see `[PyPy 7.3.9....]`

# Install the required packages
python -m pip install -U -r requirements.txt

# Run the tests for a specific task where X in [1, 3]
pytest test -m task_X

# Run the tests for all tasks 
python -m pytest test  # (`python -m` can be omitted)

# Restore python version when you are done
pyenv global system
```
