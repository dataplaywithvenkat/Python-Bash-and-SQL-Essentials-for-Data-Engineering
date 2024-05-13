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

- **Understanding Assignment Statements**
  - Assignment statements in Python assign a value to a variable.
  - Variables are names that point to pieces of data in Python.

- **Variable Naming Rules**
  - Variable names must start with a letter or underscore.
  - Subsequent characters can be letters, numbers, or underscores.
  - Python variable names are case-sensitive.

- **Assigning Values to Variables**
  - Use the assignment operator (`=`) to assign a value to a variable.
  - Example: `day = 1`

- **Using Variables in Expressions**
  - Variables can be used in expressions for arithmetic operations.
  - Example: `result = day + 1`

- **Assigning Multiple Values**
  - Multiple variables can be assigned to the same value by chaining them together.
  - Use commas to assign multiple variables to multiple values.
  - Example: `a, b = 1, 2`

- **Updating Variables**
  - Variables can be updated by assigning the result of an expression back to the variable.
  - Example: `a = a + 1` or `a += 1`

- **Augmented Assignment**
  - Python provides shorthand operators for common update operations.
  - Example: `a += 1` is equivalent to `a = a + 1`.

### Best Practices
- Choose descriptive variable names to enhance code readability.
- Avoid overusing single-letter variable names except in cases of well-known conventions.


## Import Statements in Python

- **Understanding Import Statements**
  - Import statements are used to bring modules into a Python program's running memory.
  - Modules can be imported from the Python standard library, installed libraries using pip, or self-written modules.

- **Basic Import Syntax**
  - Use the `import` keyword followed by the module name to import a module.
  - Example: `import os`

- **Accessing Functions and Sub-modules**
  - Functions and sub-modules are accessed using dot syntax.
  - Example: `os.getcwd()` to access the `getcwd` function in the `os` module.

- **Importing Specific Sub-modules or Methods**
  - Use the `from ... import ...` syntax to import specific sub-modules or methods.
  - Example: `from os import path` to import the `path` sub-module of the `os` module.

- **Importing All Sub-modules and Functions**
  - It's possible to import all sub-modules and functions using the `import *` syntax, but it's generally not recommended.

- **Alias Modules or Functions**
  - Modules or functions can be aliased during import using the `as` syntax.
  - Example: `import pandas as pd` to import the `pandas` module as `pd`.

### Best Practices
- Import only the necessary modules, sub-modules, or functions to keep the code clean and efficient.
- Use descriptive aliases when necessary for clarity and brevity in code.


## Other Simple Statements in Python

- **Understanding Simple Statements**
  - Simple statements are basic units of code execution in Python.
  - In addition to expression statements, assignment statements, and import statements, there are other simple statements to explore.

- **Types of Simple Statements**
  - Besides the commonly used statements, there are others like Pass, Delete, Return, Yield, Break, Continue, Global, Nonlocal, Raise, and Assert statements.

- **Future Statements**
  - Future statements allow importing features from a later version of Python into the current version, useful for migrating code between versions.

- **Raise Statements**
  - Raise statements are used to raise exceptions in Python.
  - Syntax: `raise ExceptionType(message)`.
  - They halt program execution and display an exception traceback if not handled.

- **Assert Statements**
  - Assert statements confirm that a condition in the program is true.
  - Syntax: `assert condition, message`.
  - They raise an AssertionError if the condition is false.

- **Best Practices**
  - Raise and assert statements are primarily used during development and debugging.
  - Disable assert statements in production code to avoid performance overhead.


## Lesson Reflection

### Lesson Summary

This lesson covers additional Python simple statements beyond expressions, assignments, and imports. Specifically it introduces exceptions, raise statements to trigger exceptions, and assert statements to validate conditions.

### Key points:

Exceptions will stop execution of a program when an error occurs

Raise statements manually raise exception errors

Assert statements validate conditions, raising errors if they fail

These mechanisms help handle errors and validate assumptions in code

### Reflection Questions

What are some common exceptions you might encounter when writing Python code?

When might you want to manually raise an exception in your code?

How could you use assert statements to validate the inputs to a function?

What exception handling code could you add to make your programs more robust?

Why is it useful to raise errors and handle exceptions in programming?

### Challenges

Add a raise statement to throw a custom exception when invalid parameters are passed to a function

Use try/except blocks to catch errors and handle them gracefully

Validate numeric inputs to functions with assert statements

Research built-in Python exceptions and choose ones relevant for a program you are writing

Handle possible exceptions from importing external libraries or modules

### Code Examples

```python
import pandas as pd

def analyze_series(s):
    """Analyze pandas Series.
    
    Demonstrates assertions and exception handling.
    """
    
    # Validate inputs
    assert isinstance(s, pd.Series), "Input must be a pandas Series"  

    try:
        # Attempt processing 
        mean = s.mean()  
        median = s.median()

    # Catch errors    
    except Exception as e:   
        # Manually raise exception
        raise ValueError("Error analyzing series") from e  

    # Assert reasonable results       
    assert (mean > 0) & (median > 0), "Mean and median are invalid!"
    
    return mean, median
    
s = pd.Series([1, 2, 3])
analyze_series(s)
```

## key terms
### Function
A named block of reusable code that can be executed multiple times. Defined using the `def` keyword.

### Parameters
Variables that serve as inputs to a function. Specified within the parentheses in the function definition.

### Return Statement
Returns a value from the function. Used to define the output of a function.

### Default Parameter Value
A value automatically assigned to a parameter if no argument is passed for that parameter in the function call. Defined using `=` in the function definition.

### Code Block
The lines of code associated with and controlled by a programming statement. Indented under the statement.


## Compound Statements in Python


## If Statements in Python

## While Loops in Python

## Functions in Python
