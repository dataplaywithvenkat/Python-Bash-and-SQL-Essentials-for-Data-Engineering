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

```python
# Function with two parameters 
def add_nums(num1, num2):
    sum = num1 + num2
    return sum

# Call function using parameters  
result = add_nums(5, 3)
print(result)

# Function with default parameter
def hello(name="John"):
    print("Hello " + name)

hello() # Uses default name 
hello("Jane") # Overrides default

# Function with code block
def print_lines():
    print("Line 1")
    print("Line 2")
    print("Line 3")
    
print_lines()

```


## Compound Statements in Python
# Evaluating to True or False

Python has a number of operations that evaluate as one of the special values `True` or `False`. These include comparison operations, boolean operations, and object evaluations.

## Comparison Operations

Comparison can be made either by value or identity. Comparing by value is more generalized than comparison by identity. The comparison operators that compare by value are:

- `==` Equals
- `!=` Not Equals
- `<` Less Than
- `<=` Less Than or Equal
- `>` Greater Than
- `>=` Greater Than or Equal

In most cases, two objects that are of different types will always evaluate as not equal. For example, the comparison `1 == 'b'` will evaluate as `False`, and `1 != 'b'` will evaluate as `True`. One notable exception to this is numeric types, such as integers and floating-point numbers. The comparison `1 == 1.0` will evaluate to `True`, and `1 != 1.0` will evaluate to `False`.

Run the code below to see the results of some equality comparisons. You can also try changing the values and running it again.

```python
# Example equality comparisons
print(1 == 'b')   # False
print(1 != 'b')   # True
print(1 == 1.0)   # True
print(1 != 1.0)   # False

# Try more comparisons
print(10 < 20)    # True
print(10 <= 10)   # True
print(5 > 3)      # True
print(5 >= 8)     # False

```
The order comparisons, those that test greater or less than values, will generally raise an error if the objects compared are of different types. A notable exception, again, is numeric types. The comparison `3.0 >= 2` will result in `True`. The order of objects depends on the type of objects being considered. For example, text (type string) uses lexicographic order and numeric types use numeric order.

Order comparison can be chained with multiple operators. For example, `1 < 2 <= 3` will result in `True`. Try running the examples below:

```python
# Example order comparisons
print(3.0 >= 2)         # True
print('apple' < 'bat')  # True
print('car' > 'bat')    # True

# Chained comparisons
print(1 < 2 <= 3)       # True
print(1 < 2 > 1)        # True
print(3 > 2 < 4)        # True

# Try more comparisons
print(5 <= 5 < 6)       # True
print(7 >= 8 < 10)      # False
print('abc' < 'abcd')   # True

```
The comparison operators which compare by identity are `is` and `is not`. They are most commonly used to compare against the special object `None`.

```python
# Example identity comparisons
a = None
b = None
c = 5

print(a is None)        # True
print(b is None)        # True
print(c is None)        # False

print(a is not None)    # False
print(c is not None)    # True

# Try more comparisons
x = []
y = x
z = []

print(x is y)           # True (both x and y refer to the same object)
print(x is z)           # False (x and z refer to different objects, even though they are both empty lists)

d = 10
e = 10
print(d is e)           # True (integers with the same value often refer to the same object in memory)
```
## Membership Operations

Some objects in Python can contain others. For example, the word `"Henry"` (of type string) contains the letter `"r"` (also a string). The `in` operator tests for this type of membership. The expression `"r" in "Henry"` will return `True`, and `"b" in "Henry"` will return `False`.

```python
# Example membership operations
print("r" in "Henry")   # True
print("b" in "Henry")   # False

# Try more membership tests
print("e" in "Henry")   # True
print("H" in "Henry")   # True
print("z" in "Henry")   # False
print("Hen" in "Henry") # True

# Membership in other types
print(2 in [1, 2, 3])   # True
print(4 in [1, 2, 3])   # False
print("apple" in ["apple", "banana", "cherry"]) # True
print("pear" in ["apple", "banana", "cherry"])  # False
```
## Boolean Operations

Boolean operations are based on boolean math, which you may have learned in a mathematics or philosophy course. The operators are `and`, `or`, and `not`. The first two take two operands, the last one takes one operand. 

- The `and` operator returns `True` if both of its operands evaluate as `True` and `False` if either evaluates to `False`.
- The `or` operator evaluates to `True` if either of its operands evaluates as `True` and `False` if they are both `False`.
- The `not` operator returns `False` if its operand evaluates to `True` and `True` otherwise.

You can make more complex logical operations by nesting boolean operations in parentheses. The expression `(False and False) or (not False)` evaluates to `True`, as `not False` is `True`.

```python
# Example boolean operations
print(True and True)    # True
print(True and False)   # False
print(False or True)    # True
print(False or False)   # False
print(not True)         # False
print(not False)        # True

# Complex boolean operation
print((False and False) or (not False))  # True

# Try more boolean operations
print((True or False) and (not False))   # True
print((True and False) or (not True))    # False
print(not (False or True))               # False
print((not (True and True)) or (False))  # False
```
## Object Evaluations

All objects (everything) in Python evaluate as `True` or `False`. This means you can use them in places where you would test for `True` or `False`, such as in Boolean operations. Generally, most Python objects evaluate as `True`. The exceptions are:

- Numeric types that equal zero, such as `0` or `0.0`.
- The constants `False` and `None`.
- Anything that has a length of zero. This includes the empty string, `""`.

```python
# Example object evaluations
print(bool(0))          # False
print(bool(0.0))        # False
print(bool(False))      # False
print(bool(None))       # False
print(bool(""))         # False
print(bool([]))         # False
print(bool({}))         # False

# Objects that evaluate to True
print(bool(1))          # True
print(bool(3.14))       # True
print(bool(True))       # True
print(bool("Hello"))    # True
print(bool([1, 2, 3]))  # True
print(bool({"key": "value"})) # True
```

# If, Else, Elif Statements in Python

In this lesson, you will learn the syntax of an `if` statement, the `else` keyword, and `elif` blocks. Let's look at `if` statements in a Jupyter Notebook. A notebook is composed of cells.

## If Statements

We can write multiple statements in a code cell, much as you would in a file, but then we can execute that code cell and get the output right away, much like in an interactive session. The `if` statement uses the keyword `if` followed by an expression. If that expression evaluates to `True`, then the controlled code block is executed; if it evaluates to `False`, then that block is skipped. Here, our expression is actually the keyword `True` or the constant `True`. We can see if we execute it, that both the control block and the code after the `if` statement are executed.

## Else Keyword

If the expression evaluates to `False`, then the controlled code block is skipped. The `else` keyword is used to have an alternative code block to the main controlled one. Basically, this is executed if the expression controlling the first code block is `False`. Here we have a variable named `score`, and we say that if that score is greater than three, we run the first control block; in all other cases, we'll run the second control block, which is controlled by the `else` statement.

```python
# If and else example
score = 1
if score > 3:
    print("Score is greater than three.")
else:
    print("Score is three or less.")  # This block is executed because score is 1

score = 4
if score > 3:
    print("Score is greater than three.")  # This block is executed because score is 4
else:
    print("Score is three or less.")
```
## Elif Blocks

We can nest if statements within the else context to have more control over creating alternatives. Here we have a nested if statement that says if the variable is greater than three, it will print this message.

```python
# Nested if example
score = 3
if score > 3:
    print("Score is greater than three.")
else:
    if score == 3:
        print("Score is exactly three.")
    else:
        print("Score is less than three.")  # This block is executed because score is 3
```

## While Loops in Python


