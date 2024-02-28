---
title: Week 3
layout: default
parent: Python Tutorial 
grand_parent: Tutorials
nav_order: 3
---

# Week 3: Lists and Tuples
Session 1 (2 hours)
{: .fs-6 .fw-300 }

- **Lists**: Learn about lists, a versatile data structure in Python that can hold elements of different types.
- **List operations**: Explore various operations on lists such as indexing, slicing, appending, and extending.
- **Tuples**: Understand tuples, which are similar to lists but immutable.

**Example Code Snippets**:
```python
# Example code for lists
fruits = ["apple", "banana", "cherry", "orange"]
print(fruits[0])  # Accessing elements by index
print(fruits[1:3])  # Slicing
fruits.append("grape")  # Appending
print(fruits)
```

## Exercises
1. Write a Python program to count the number of elements in a list. (Easy)
2. Write a function to find the largest element in a list. (Medium)
3. Write a program to remove duplicates from a list. (Medium)
4. Write a function to reverse a list. (Easy)
5. Write a program to find the sum of all elements in a list. (Easy)
6. Write a Python program to sort a list of tuples based on the second element. (Hard)
7. Write a function to check if two lists are equal. (Medium)
8. Write a program to merge two lists into a single list. (Medium)
9. Write a Python program to shuffle a list randomly. (Hard)
10. Write a function to check if a list is palindrome or not. (Medium)

## Exercise Solutions
1. ```python
   fruits = ["apple", "banana", "cherry", "orange"]
   print("Number of elements:", len(fruits))
   ```
2. ```python
   def find_largest(lst):
       return max(lst)
   
   numbers = [5, 10, 15, 20]
   print("Largest element:", find_largest(numbers))
   ```
3. ```python
   fruits = ["apple", "banana", "cherry", "banana", "orange", "cherry"]
   unique_fruits = list(set(fruits))
   print("List without duplicates:", unique_fruits)
   ```
4. ```python
   numbers = [1, 2, 3, 4, 5]
   reversed_numbers = numbers[::-1]
   print("Reversed list:", reversed_numbers)
   ```
5. ```python
   numbers = [1, 2, 3, 4, 5]
   total_sum = sum(numbers)
   print("Sum of elements:", total_sum)
   ```
6. ```python
   tuples_list = [(1, 2), (3, 1), (5, 4), (7, 6)]
   sorted_tuples = sorted(tuples_list, key=lambda x: x[1])
   print("Sorted list of tuples:", sorted_tuples)
   ```
7. ```python
   list1 = [1, 2, 3]
   list2 = [1, 2, 3]
   if list1 == list2:
       print("Lists are equal")
   else:
       print("Lists are not equal")
   ```
8. ```python
   list1 = [1, 2, 3]
   list2 = [4, 5, 6]
   merged_list = list1 + list2
   print("Merged list:", merged_list)
   ```
9. ```python
   import random
   numbers = [1, 2, 3, 4, 5]
   random.shuffle(numbers)
   print("Shuffled list:", numbers)
   ```
10. ```python
    def is_palindrome(lst):
        return lst == lst[::-1]
    
    numbers = [1, 2, 3, 2, 1]
    if is_palindrome(numbers):
        print("List is a palindrome")
    else:
        print("List is not a palindrome")
    ```

Session 2 (2 hours)
{: .fs-6 .fw-300 }

- **Tuples vs Lists**: Understand the differences between tuples and lists and when to use each.
- **List comprehensions**: Learn about list comprehensions for creating lists based on existing lists or other iterables.
- **Tuple unpacking**: Explore tuple

 unpacking, a feature that allows you to assign values from a tuple to multiple variables.

**Example Code Snippets**:
```python
# Example code for list comprehensions
squares = [x**2 for x in range(5)]
print("Squares:", squares)

# Example code for tuple unpacking
coordinates = (3, 4)
x, y = coordinates
print("x-coordinate:", x)
print("y-coordinate:", y)
```

## Exercises
1. Write a Python program to find the intersection of two lists. (Medium)
2. Write a function to flatten a nested list. (Hard)
3. Write a program to convert a list of characters into a string. (Easy)
4. Write a Python program to find the second smallest number in a list. (Medium)
5. Write a function to remove the nth index element from a list. (Easy)
6. Write a program to find the union of two lists. (Medium)
7. Write a Python program to create a tuple with different data types. (Easy)
8. Write a function to check if a list contains any duplicates. (Medium)
9. Write a Python program to extract the unique elements from a list of lists. (Hard)
10. Write a function to find the frequency of occurrence of an element in a list. (Medium)

## Exercise Solutions
1. ```python
   list1 = [1, 2, 3, 4, 5]
   list2 = [4, 5, 6, 7, 8]
   intersection = list(set(list1) & set(list2))
   print("Intersection:", intersection)
   ```
2. ```python
   def flatten(lst):
       return [item for sublist in lst for item in sublist]
   
   nested_list = [[1, 2], [3, 4, 5], [6, 7, 8, 9]]
   flattened_list = flatten(nested_list)
   print("Flattened list:", flattened_list)
   ```
3. ```python
   characters = ['a', 'b', 'c', 'd']
   string = ''.join(characters)
   print("String:", string)
   ```
4. ```python
   numbers = [5, 3, 8, 2, 1, 7]
   sorted_numbers = sorted(numbers)
   second_smallest = sorted_numbers[1]
   print("Second smallest:", second_smallest)
   ```
5. ```python
   def remove_nth_element(lst, n):
       del lst[n]
       return lst
   
   numbers = [1, 2, 3, 4, 5]
   print("List after removing 3rd element:", remove_nth_element(numbers, 2))
   ```
6. ```python
   list1 = [1, 2, 3]
   list2 = [3, 4, 5]
   union = list(set(list1) | set(list2))
   print("Union:", union)
   ```
7. ```python
   mixed_tuple = (1, "apple", True, 3.14)
   print("Mixed tuple:", mixed_tuple)
   ```
8. ```python
   numbers = [1, 2, 3, 2, 4, 5]
   duplicates = any(numbers.count(element) > 1 for element in numbers)
   if duplicates:
       print("List contains duplicates")
   else:
       print("List does not contain duplicates")
   ```
9. ```python
   list_of_lists = [[1, 2], [2, 3, 4], [1, 5]]
   unique_elements = set(item for sublist in list_of_lists for item in sublist)
   print("Unique elements:", unique_elements)
   ```
10. ```python
    def frequency(lst, element):
        return lst.count(element)
    
    numbers = [1, 2, 3, 2, 4, 2, 5]
    print("Frequency of 2:", frequency(numbers, 2))
    ```
