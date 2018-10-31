# Introduction to Data Science - Lab 1

Hi there, welcome to our first lab. Labs are meant to give you practical data science skills. We will be using Python, a popular data science programming language in the labs, homeworks, and projects. As part of Homework 0, you should have already setup Python, IPython and Jupyter notebooks, so it's time to get started!

## Executing your first program

Now it's time to run python! Open a terminal and execute:

```
$ python
```

You'll see something like that:

```
$ python
Python 3.5.1 |Continuum Analytics, Inc.| (default, Jun 15 2016, 16:14:02)
[GCC 4.2.1 Compatible Apple LLVM 4.2 (clang-425.0.28)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>>
```
What does this tell us? It shows us the version number of Python (3.5.1), and we can see that we've installed the Anaconda version from Continuum Analytics. At the end of this statement, you see the thre >>> signs: these indicate a promt, but it looks different from your console promt ($), to indicate you're in an interactive python environment.

There are two fundamental ways you can run Python: in interactive mode (what we're doing here) or in batch mode. In interactive mode you write your program interactively, i.e., each new statement is interpreted as you type it. If you just run ```python``` without any other parameter, you enter the **interactive** mode. Let's write our very first program:

```
>>> print("Hello World!")
Hello World!
```

"Hello World!" is by tradition the very first program that you should write in a new programming language! And see, when we instructed python to print the text "Hello World!", it did just that.

So, let's briefly take that statement apart: it contains a call to the "print" function and passes a parameter to that print function, the string "Hello World!". Given that information, python knows you want to print the string, and it does exactly that.
Print is a built-in function of python, there are several built-in functions, which you can check out [here](https://docs.python.org/3/library/functions.html).

Let's define our first variable. Type

```
>>> my_string_var = "Are you still spinning?"
```

This statement is executed without any feedback. What you're doing here, intuitively, is that first, you create a new variable of type string with the name ```my_string_var```, and then you assign a value to it, "Are you still spinning?". We now can print this variable:

```
>>> print(my_string_var)
Are you still spinning?
```

which produces the result we expected!

There are many different types of variables, not only strings. For example, Python has three different data types for numbers (integers, floats - that represent real numbers, and complex). Check out the details about the built-in data types [here](https://docs.python.org/3/library/stdtypes.html).

Let's start with a simple example:

```
>>> a = 3
>>> b = 2.5
>>> c = a + b
>>> print(c)
5.5
```

Here we've created three variables (`a, b, c`) and executed an operation, the addition of `a` and `b` using the `+` operator, which we have then assigned to `c`. Finally, we've printed `c`.

The data types of `a` and `b`, however, are subtly different. `a` is an integer and `b` is a float. We can check the data type of any variable using the `type()` function:

```
>>> a = 3
>>> type(a)
<class 'int'>
>>> b = 2.5
<class 'float'>
>>> c = "hello"
>>> type(c)
<class 'str'>
```

Python supports many operations, including divisions, type conversions, etc. - we'll explore those soon.

### Exercise: Data types and operations

Play around with data types and operations. Try the following things:

 * Define a variable and assign an integer and a float. Define a new variable and assign the sum of the previous variables. What's the data type of the third variable?
 * Reassign a variable with a different data type, e.g., take one of your numerical variables and assign a string to it. What's the new data type?
 * Try what happens if you try to add a string to a string?
 * Try what happens if you add a string to a float or an integer.


## Writing code in a file

For now, though, let's look at another way to run python: by executing a file. Exit the interactive environment, by calling the exit function:

```
exit()
```

Now, open up your favorite text editor (if you don't have one, check out, e.g., [Atom](https://atom.io/)) and create a new file called "first_steps.py". We've created such a file for you [here](first_steps.py).

You can also copy and paste this code into the file:

```python
def doubleNumber(a):
    # btw, here is a comment! Use the # symbol to add comments or temporarily remove code
    # shorthand operator for 'a = a * 2'
    # also btw - the indentation here matters!
    a *= 2
    return a;

print(doubleNumber(3))
print(doubleNumber(14.22))
```

Here we've also defined or first own function! We'll go into details about functions at a later time. For now, just notice that the indentation matters!

Now, run

```
$ python first_steps.py
6
28.44
```

What happened here? Python executed the commands in the file, and then terminated. You saw the result, but it was not interactive anymore, but executed in a couple of milliseconds.

Larger and bigger programs are commonly written using source code files and are not run interactively. They will read data from files and wait for user input, etc.

### Exercise: Running Programs

 * Create a new file and use the simple function as a template. Modify the code to divide numbers by two instead of doubling them.
 * Try what happens if you change the indentation. Can you guess what's happening?
 * Try what happens if you print `a` at the very end of the program. Can you explain what's going on?


## Jupyter Notebooks
We've prepared a notebook for the rest of this class. You should have already downloaded it as part of HW0. If not, get it [here](lab-1-notebook.ipynb), change to the appropriate directory, and run

```
$ jupyter notebook
```

We're switching over to notebooks now!
