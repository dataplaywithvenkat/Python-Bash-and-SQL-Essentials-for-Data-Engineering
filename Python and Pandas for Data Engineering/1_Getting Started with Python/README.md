# Setting up your Environment

## Key Terms
Package - Python code bundled together for distribution and installation

Module - Python code saved to a file for reuse

venv - create a virtual environment

activate - activate/enter the virtual environment

pip install - install packages into the active virtual environment

pip list - list packages installed in the current environment

pip freeze - output installed packages to a requirements file

deactivate - exit the active virtual environment

```python
# Create virtual environment 
python3 -m venv my_env

# Activate virtual environment
source my_env/bin/activate 

# Install packages to virtual environment
pip install pandas

# List packages installed in environment
pip list 

# Save installed packages to requirements file
pip freeze > requirements.txt

# Deactivate virtual environment 
deactivate
```

## Installing Packages with pip in Python
In this lesson, I learned about package installation using pip. Here are the key points:

- **What is a Package?**
  - Python code can be run interactively or from files. When code is saved to a file for reuse, it's called a module.
  - Modules or groups of modules bundled together for distribution are referred to as packages.
  - Python's Standard Library contains packages usable in any Python program.
  - Additionally, there's a vast ecosystem of third-party packages available on the Python Package Index (PyPI).

- **Introduction to pip**
  - Pip is the default package installer for Python, used for managing package installations.
  - It downloads and installs packages from PyPI by default, but it can be configured for other sources.

- **Usage**
  - Pip is generally accessed via `python -m pip` or as a separate standalone command.
  - `pip help` lists all available commands and options.
  - Key commands: `list`, `install`, and `uninstall`.

- **Installing and Managing Packages**
  - The `install` command installs packages. For example, `pip install pytest`.
  - Pip installs dependencies automatically.
  - `pip list` shows installed packages.
  - Use `pip uninstall` followed by the package name to remove packages.

- **Installing Specific Versions**
  - To install a specific version, use double equal signs. For example, `pip install pytest==5.0.1`.
  - Upgrading packages: Either uninstall and reinstall or use `pip install --upgrade`.


## Saving Requirements File in Python
In this lesson, we'll cover how to save the current state of your Python package installation to a requirements file, along with uninstalling packages listed in a requirements file and installing packages using it.

- **Why Save a Requirements File?**
  - Saving a record of installed packages makes your project portable across different machines.
  - It ensures that others can reproduce your environment and run your project seamlessly.

- **Creating a Requirements File**
  - The `pip freeze` command displays installed packages in a format suitable for a requirements file.
  - Redirect the output of `pip freeze` to a file using the rightward arrow (`>`).
  - Conventionally, name the file `requirements.txt`.

- **Using Requirements File**
  - To install packages listed in a requirements file, use `pip install -r requirements.txt`.
  - This command installs all listed packages and their dependencies.
  - To uninstall packages listed in the file, use `pip uninstall -r requirements.txt`.

- **Best Practices**
  - Creating and using requirements files is standard practice for managing project dependencies.
  - It ensures consistency across environments and simplifies project setup for collaborators or new environments.


## Creating and Using a Python Virtual Environment

In this lesson, we'll cover the creation and utilization of Python virtual environments, including activating, installing packages, and deactivating them.

- **Why Use Virtual Environments?**
  - By default, installing packages affects the user environment, leading to shared dependencies across projects.
  - This can cause issues with package version conflicts and wasted disk space due to unnecessary installations.

- **Introduction to Python Virtual Environments**
  - Python virtual environments isolate dependencies for each project, solving the issues of shared environments.
  - They allow for project-specific dependencies without affecting the global Python installation.

- **Creating a Virtual Environment**
  - Virtual environments are created using the `venv` module provided in Python 3.5 and later.
  - Use the `python -m venv <path>` command to create a virtual environment in the specified location.

- **Activating and Using a Virtual Environment**
  - Once created, activate the virtual environment using the `source` command with the `activate` script.
  - Activated environments isolate package installations to the current project only.

- **Installing Packages**
  - Packages installed while in a virtual environment are limited to that environment.
  - Use `pip list` to view installed packages, reflecting only those installed within the environment.

- **Deactivating and Leaving a Virtual Environment**
  - To deactivate the environment, simply use the `deactivate` command provided by the `venv` module.

## Best Practices
- Store virtual environments centrally or within project directories, depending on preference.
- Utilize virtual environments for each project to maintain dependency isolation and ensure project portability.

## Expression Statements in Python
- **Introduction to IPython**
  - IPython is an enhanced interactive Python shell, providing additional features over the default Python shell.
  - It offers a more robust and feature-rich environment for interactive Python programming.

- **Installation**
  - IPython can be installed using pip, the Python package installer.
  - Use `pip install ipython` to install IPython on your system.

- **Running IPython**
  - Once installed, you can open the IPython shell by typing `ipython` in your command line interface.

- **Interactive Code Execution**
  - In the IPython shell, statements are executed interactively, and the return value is displayed immediately.
  - You can execute Python expression statements directly in the IPython shell.

- **Working with Expressions**
  - Python expressions are pieces of code that evaluate to a value.
  - Expression statements are simple statements containing only expressions.

- **Examples of Expressions**
  - Perform arithmetic operations like addition, subtraction, multiplication, division, exponentiation, and modulus.
  - Use parentheses to group expressions for precedence.

- **Interactive Usage**
  - Typing a single object in the IPython shell echoes its value as output, useful for inspecting objects.


## Assignment Statements in Python

## Import Statements in Python

## Other Simple Statements in Python

## Compound Statements in Python

## If Statements in Python

## While Loops in Python

## Functions in Python
