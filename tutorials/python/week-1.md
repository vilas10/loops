---
title: Week 1
layout: default
parent: Python Tutorial 
grand_parent: Tutorials
nav_order: 1
---

# Week 1: Introduction to Python
## Session 1 (2 hours):
- **Introduction to Python**: Python is a high-level programming language known for its simplicity and readability. It is widely used in various domains such as web development, data science, artificial intelligence, etc.
- **Setting up Python environment**: Install Python on your computer and choose an Integrated Development Environment (IDE) like PyCharm or Visual Studio Code to write and run Python code.
- **Basic syntax**: Learn about variables, data types (integers, floats, strings, booleans), basic arithmetic operators (+, -, *, /), and how to print output using the print statement.

**Example Code Snippets**:
```python
# Example code for variables and data types
x = 5
y = 3.14
name = "Alice"
is_student = True

# Example code for arithmetic operators
sum_result = x + y
difference_result = x - y
product_result = x * y
quotient_result = x / y

# Example code for printing output
print("Sum of x and y:", sum_result)
```

**Exercises**:
1. Print "Hello, World!" to the console. (Easy)
2. Calculate the area of a rectangle with length 5 and width 3. (Easy)
3. Convert a temperature of 25 degrees Celsius to Fahrenheit. (Medium)
4. Check if a number is even or odd and print the result. (Medium)
5. Swap the values of two variables x and y. (Hard)
6. Calculate the sum of digits of a three-digit number. (Hard)
7. Print the Fibonacci series up to 10 terms. (Hard)
8. Find the maximum of two numbers x and y. (Medium)
9. Calculate the square root of a number. (Medium)
10. Check if a given string is empty or not. (Easy)

### Exercise Solutions:
1. ```python
   print("Hello, World!")
   ```
2. ```python
   length = 5
   width = 3
   area = length * width
   print("Area of rectangle:", area)
   ```
3. ```python
   celsius = 25
   fahrenheit = (celsius * 9/5) + 32
   print("Temperature in Fahrenheit:", fahrenheit)
   ```
4. ```python
   num = 10
   if num % 2 == 0:
       print("Even")
   else:
       print("Odd")
   ```
5. ```python
   x = 5
   y = 10
   x, y = y, x
   print("Swapped values: x =", x, ", y =", y)
   ```
6. ```python
   number = 123
   sum_of_digits = sum(int(digit) for digit in str(number))
   print("Sum of digits:", sum_of_digits)
   ```
7. ```python
   n = 10
   fib_sequence = [0, 1]
   for i in range(2, n):
       fib_sequence.append(fib_sequence[-1] + fib_sequence[-2])
   print("Fibonacci series:", fib_sequence)
   ```
8. ```python
   x = 5
   y = 10
   maximum = x if x > y else y
   print("Maximum:", maximum)
   ```
9. ```python
   import math
   num = 25
   square_root = math.sqrt(num)
   print("Square root:", square_root)
   ```
10. ```python
    string = "Hello"
    if string:
        print("String is not empty")
    else:
        print("String is empty")
    ```