Functions in Python - A Comprehensive Guide
This repository is a collection of examples and explanations of various concepts related to functions in Python. Below, you will find an overview of the topics covered, including methods, arguments, parameters, default arguments, lambda functions, recursion, static and class methods, generator functions, iterators, and the purpose of map, filter, and reduce functions.

Table of Contents
Functions and Methods
Arguments and Parameters
Default Arguments
Lambda Functions
Recursive Methods
Static Methods
Class Methods
Generator Functions
Return Functions
Iterators
Map, Filter, and Reduce Functions
Functions and Methods
A function is a block of code designed to perform a specific task. A method is a function that is associated with an object. In Python, functions are defined using the def keyword.

Example:

python
Copy
Edit
def greet(name):
    print(f"Hello, {name}!")
Arguments and Parameters
Arguments are the values you pass into the function, while parameters are the variables that accept those values inside the function definition.

Example:

python
Copy
Edit
def add(a, b):  # 'a' and 'b' are parameters
    return a + b

result = add(5, 3)  # 5 and 3 are arguments
Default Arguments
A function can have default values for parameters. These default values are used if no value is provided for that parameter when the function is called.

Example:

python
Copy
Edit
def greet(name, age=25):
    print(f"Hello {name}, you are {age} years old.")

greet("Alice")  # Uses default age
Lambda Functions
A lambda function is a small anonymous function defined using the lambda keyword. It can have any number of arguments but only one expression.

Example:

python
Copy
Edit
multiply = lambda x, y: x * y
print(multiply(4, 5))  # Output: 20
Recursive Methods
A recursive method is a function that calls itself to solve smaller instances of the same problem.

Example:

python
Copy
Edit
def factorial(n):
    if n == 1:
        return 1
    else:
        return n * factorial(n - 1)

print(factorial(5))  # Output: 120
Static Methods
A static method is a method that belongs to the class rather than an instance of the class. It is defined using the @staticmethod decorator.

Example:

python
Copy
Edit
class Calculator:
    @staticmethod
    def add(a, b):
        return a + b

print(Calculator.add(10, 20))  # Output: 30
Class Methods
A class method is a method that is bound to the class rather than an instance of the class. It is defined using the @classmethod decorator.

Example:

python
Copy
Edit
class Person:
    name = "John"

    @classmethod
    def greet(cls):
        print(f"Hello, {cls.name}!")

Person.greet()  # Output: Hello, John!
Generator Functions
A generator function is a function that returns an iterator and is defined using the yield keyword. It generates values one at a time when iterated over.

Example:

python
Copy
Edit
def count_up_to(n):
    count = 1
    while count <= n:
        yield count
        count += 1

for number in count_up_to(5):
    print(number)
Return Functions
A function can return another function, allowing for functional programming and closures.

Example:

python
Copy
Edit
def outer_function(x):
    def inner_function(y):
        return x + y
    return inner_function

add_five = outer_function(5)
print(add_five(3))  # Output: 8
Iterators
An iterator is an object that represents a stream of data. It is used to iterate over elements, such as in a for loop.

Example:

python
Copy
Edit
numbers = [1, 2, 3]
iterator = iter(numbers)

print(next(iterator))  # Output: 1
print(next(iterator))  # Output: 2
Map, Filter, and Reduce Functions
Map: Applies a function to all items in an input list and returns a new list with the results.

Example:

python
Copy
Edit
numbers = [1, 2, 3]
squared = list(map(lambda x: x**2, numbers))
print(squared)  # Output: [1, 4, 9]
Filter: Filters the input list based on a function that returns True or False.

Example:

python
Copy
Edit
numbers = [1, 2, 3, 4]
even_numbers = list(filter(lambda x: x % 2 == 0, numbers))
print(even_numbers)  # Output: [2, 4]
Reduce: Applies a rolling computation to the items of a sequence. It is available in the functools module.

Example:

python
Copy
Edit
from functools import reduce

numbers = [1, 2, 3, 4]
result = reduce(lambda x, y: x + y, numbers)
print(result)  # Output: 10# Functions
GitHub is a leading platform for version control and collaboration, widely used in software development and project management. Its core functions streamline teamwork, code management, and project tracking.   
