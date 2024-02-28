---
title: Week 2
layout: default
parent: Python Tutorial 
grand_parent: Tutorials
nav_order: 2
---

# Week 2: Control Structures and Functions
## Session 1 (2 hours):
- **Conditional statements**: Use if, elif, and else statements for decision-making based on conditions.
- **Loops**: Learn about for and while loops for iterating over sequences of elements.
- **Functions**: Define reusable blocks of code using functions with parameters and return statements.

**Example Code Snippets**:
```python
# Example code for conditional statements
x = 10
if x > 0:
    print("Positive")
elif x == 0:
    print("Zero")
else:
    print("Negative")

# Example code for loops
for i in range(5):
    print("Iteration", i)

# Example code for functions
def square(x):
    return x * x

result = square(3)
print("Square of 3:", result)
```

## Exercises
1. Write a Python function to calculate the factorial of a given number. (Medium)
2. Print the multiplication table of a given number. (Easy)
3. Check if a number entered by the user is prime or not. (Medium)
4. Write a function to check if a string is a palindrome. (Medium)
5. Generate a list of even numbers from 1 to 100. (Hard)
6. Implement a simple calculator program using functions for addition, subtraction, multiplication, and division. (Hard)
7. Find the minimum of three numbers entered by the user. (Medium)
8. Write a function to calculate the average of elements in a list. (Medium)
9. Check if a given year is a leap year or not. (Easy)
10. Reverse a given string using a loop. (Easy)

## Exercise Solutions
1. ```python
   def factorial(n):
       if n == 0:
           return 1
       else:
           return n * factorial(n-1)
   
   result = factorial(5)
   print("Factorial of 5:", result)
   ```
2. ```python
   num = 5
   for i in range(1, 11):
       print(num, "x", i, "=", num * i)
   ```
3. ```python
   def is_prime(n):
       if n <= 1:
           return False
       for i in range(2, int(n**0.5) + 1):
           if n % i == 0:
               return False
       return True
   
   number = 17
   if is_prime(number):
       print(number, "is prime")
   else:
       print(number, "is not prime")
   ```
4. ```python
   def is_palindrome(string):
       return string == string[::-1]
   
   text = "radar"
   if is_palindrome(text):
       print(text, "is a palindrome")
   else:
       print(text, "is not a palindrome")
   ```
5. ```python
   even_numbers = [num for num in range(1, 101) if num % 2 == 0]
   print("Even numbers:", even_numbers)
   ```
6. ```python
   def add(a, b):
       return a + b
   
   def subtract(a, b):
       return a - b
   
   def multiply(a, b):
       return a * b
   
   def divide(a, b):
       return a / b
   
   num1 = 10
   num2 = 5
   print("Sum:", add(num1, num2))
   print("Difference:", subtract(num1, num2))
   print("Product:", multiply(num1, num2))
   print("Quotient:", divide(num1, num2))
   ```
7. ```python
   numbers = [10, 5, 15]
   print("Minimum:", min(numbers))
   ```
8. ```python
   def average(numbers):
       return sum(numbers) / len(numbers)
   
   nums = [5, 10, 15, 20]
   print("Average:", average(nums))
   ```
9. ```python
   year = 2024
   if year % 4 == 0 and (year % 100 != 0 or year % 400 == 0):
       print(year, "is a leap year")
   else:
       print(year, "is not a leap year")
   ```
10. ```python
    text = "hello"
    reversed_text = ""
    for char in text:
        reversed_text = char + reversed_text
    print("Reversed:", reversed_text)
    ```

## Session 2 (30 mins):
- **Nested loops**: Understand how to use loops within loops (nested loops) for more complex iterations.
- **Break and continue**: Learn about the break and continue statements for controlling loop execution.
- **Function arguments**: Explore different ways of passing arguments to functions, including positional arguments, keyword arguments, and default values.

**Example Code Snippets**:
```python
# Example code for nested loops
for i in range(3):
    for j in range(2):
        print(i, j)

# Example code for break and continue
for i in range(5):
    if i == 3:
        break
    print(i)

# Example code for function arguments
def greet(name, greeting="Hello"):
    print(greeting, name)

greet("Alice")
greet("Bob", "Hi")
```

## Exercises
1. Write a Python program to print a pattern using nested loops. (Hard)
2. Write a function to find the factorial of a number using recursion. (Medium)
3. Print all prime numbers between 10 and 50. (Medium)
4. Write a program to find the sum of all elements in a nested list. (Hard)
5. Implement a function to calculate the power of a number using recursion. (Medium)
6. Write a program to print all Armstrong numbers between 1 and 1000. (Hard)
7. Implement a function to calculate the factorial of a number using an iterative approach. (Medium)
8. Write a Python program to display the Fibonacci sequence using recursion. (Medium)
9. Print the following pattern using nested loops:
   ```
   1
   1 2
   1 2 3
   1 2 3 4
   1 2 3 4 5
   ```
   (Medium)
10. Write a function to check if a number is a perfect number or not. (Hard)

## Exercise Solutions
1. ```python
   for i in range(5):
       for j in range(i + 1):
           print("*", end=" ")
       print()
   ```
2. ```python
   def factorial(n):
       if n == 0:
           return 1
       else:
           return n * factorial(n-1)
   
   result = factorial(5)
   print("Factorial of 5:", result)
   ```
3. ```python
   def is_prime(n):
       if n <= 1:
           return False
       for i in range(2, int(n**0.5) + 1):
           if n % i == 0:
               return False
       return True
   
   for num in range(10

, 51):
       if is_prime(num):
           print(num)
   ```
4. ```python
   nested_list = [[1, 2], [3, 4, 5], [6, 7, 8, 9]]
   total_sum = 0
   for sublist in nested_list:
       for num in sublist:
           total_sum += num
   print("Total sum:", total_sum)
   ```
5. ```python
   def power(base, exponent):
       if exponent == 0:
           return 1
       else:
           return base * power(base, exponent - 1)
   
   print("2^3 =", power(2, 3))
   ```
6. ```python
   for num in range(1, 1001):
       num_str = str(num)
       num_digits = len(num_str)
       total = sum(int(digit)**num_digits for digit in num_str)
       if total == num:
           print(num)
   ```
7. ```python
   def factorial_iterative(n):
       result = 1
       for i in range(1, n + 1):
           result *= i
       return result
   
   result = factorial_iterative(5)
   print("Factorial of 5 (iterative):", result)
   ```
8. ```python
   def fibonacci(n):
       if n <= 1:
           return n
       else:
           return fibonacci(n-1) + fibonacci(n-2)
   
   for i in range(10):
       print(fibonacci(i), end=" ")
   ```
9. ```python
   for i in range(1, 6):
       for j in range(1, i + 1):
           print(j, end=" ")
       print()
   ```
10. ```python
    def is_perfect(n):
        divisors_sum = sum(i for i in range(1, n) if n % i == 0)
        return divisors_sum == n

    num = 28
    if is_perfect(num):
        print(num, "is a perfect number")
    else:
        print(num, "is not a perfect number")
    ```

## Session 3
- Input
- One-line If-Else
- Main Entry

### Input Function
The `input()` function in Python allows us to receive user input from the keyboard. It prompts the user with a message and waits for the user to type something and press Enter. The input is always returned as a string.

**Syntax:**
```python
user_input = input("Prompt message: ")
```

**Example:**
```python
name = input("Enter your name: ")
print("Hello,", name)
```

### One-line If-Else Statement
Python allows us to write simple `if-else` statements in a single line. This is useful for writing compact code when the condition and actions are simple.

**Syntax:**
```python
result = value_if_true if condition else value_if_false
```

**Example:**
```python
num = 5
is_even = "Even" if num % 2 == 0 else "Odd"
print(is_even)
```

### Main Entry in Python
In Python, the `if __name__ == "__main__":` block allows us to define a block of code that will only be executed when the script is run directly, not when it's imported as a module in another script. This is often used to define the main entry point of the script.

**Syntax:**
```python
def main():
    # Main program logic goes here

if __name__ == "__main__":
    main()
```

**Example:**
```python
def main():
    name = input("Enter your name: ")
    print("Hello,", name)

if __name__ == "__main__":
    main()
```

## Exercises:
1. Write a Python program that takes the user's age as input and prints "You are a minor" if the age is less than 18, otherwise prints "You are an adult".
2. Convert the following `if-else` statement into a one-line statement:
   ```python
   num = 7
   result = "Even" if num % 2 == 0 else "Odd"
   print(result)
   ```

## Exercise Solutions:
1. ```python
   age = int(input("Enter your age: "))
   status = "You are a minor" if age < 18 else "You are an adult"
   print(status)
   ```
2. ```python
   num = 7
   result = "Even" if num % 2 == 0 else "Odd"
   print(result)
   ```

