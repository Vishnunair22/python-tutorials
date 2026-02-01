# 🐍 Python Programming - Complete Study Notes

![Python](https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg)

**Comprehensive reference guide for Python fundamentals.**

---

## 📑 Table of Contents

1. [Print Function](#1-print-function)
2. [Data Types](#2-data-types)
3. [Variables](#3-variables)
4. [Keywords and Identifiers](#4-keywords-and-identifiers)
5. [Indentation](#5-indentation)
6. [User Input](#6-user-input)
7. [Type Conversion](#7-type-conversion)
8. [Literals](#8-literals)
9. [Operators](#9-operators)
10. [Conditional Statements](#10-conditional-statements)
11. [Loops](#11-loops)
12. [Exercises](#12-exercises)
13. [Projects](#13-projects)

---

## 🖨️ 1. Print Function

![Print Function](python_study_assets/python_print_function_graphic_1769916778127.png)

### Overview

The `print()` function outputs data to the standard output device (console/terminal). It converts objects to strings and displays them.

**Syntax:**
```python
print(*objects, sep=' ', end='\n', file=sys.stdout, flush=False)
```

### Basic Usage

**Printing strings:**
```python
print('Hello World')
```
**Output:**
```
Hello World
```

---

## 📦 2. Data Types

![Data Types](python_study_assets/python_data_types_graphic_1769916794933.png)

### Overview

Data types specify the kind of value a variable holds. Python has several built-in data types.

### 1. None Type (`None`)
Represents the absence of a value or a null value. It is not 0 or an empty string, it is literally "nothing".

```python
x = None
print(type(x)) # <class 'NoneType'>
```

### 2. Numeric Types
*   **int**: Whole numbers (e.g., `10`, `-5`).
*   **float**: Decimal numbers (e.g., `3.14`, `1.5e2`).
*   **complex**: Numbers with real and imaginary parts (e.g., `3 + 4j`).

### 3. Sequence Types
*   **str**: Text data (string of characters).
*   **list**: Ordered, mutable collection. `[1, 2, 3]`
*   **tuple**: Ordered, immutable collection. `(1, 2, 3)`
*   **range**: Sequence of numbers, used in loops.

### 4. Mapping Type
*   **dict**: Key-value pairs. `{'name': 'Vishnu', 'age': 25}`

### 5. Set Types
*   **set**: Unordered collection of unique items. `{1, 2, 3}`
*   **frozenset**: Immutable version of a set.

### 6. Boolean Type
*   **bool**: `True` or `False`.

> [!NOTE]
> Python is dynamically typed, so you don't need to declare types explicitly. The interpreter infers them.

---

## 🏷️ 3. Variables

![Variables](python_study_assets/python_variables_graphic_1769916816196.png)

### Definition

Variables are named memory locations storing data values. Think of them as containers.

```python
name = 'Vishnu'
age = 25
height = 5.9
```

### Dynamic Typing
Variables can change type during execution.

```python
var = 10        # int
var = "Hello"   # Now str
```

---

## 🔑 4. Keywords and Identifiers

![Keywords](python_study_assets/python_keywords_graphic_1769916832000.png)

### Keywords
Reserved words with predefined meanings (e.g., `if`, `else`, `while`, `True`).

### Identifiers
Names given to variables, functions, and classes.
*   Must start with a letter or `_`.
*   Case-sensitive (`Age` vs `age`).
*   Cannot be a keyword.

---

## 📏 5. Indentation

![Indentation](python_study_assets/python_indentation_graphic_1769917624660.png)

### Overview
Indentation defines blocks of code in Python. It is **mandatory**.

**Correct Syntax:**
```python
if True:
    print("This is indented")
    print("Part of the block")
```

**Common Error (`IndentationError`):**
```python
if True:
print("Missing indentation!") # Error!
```

---

## ⌨️ 6. User Input

![User Input](python_study_assets/python_user_input_graphic_1769916848424.png)

### Overview
Reads data from the user via the keyboard. **Always returns a string.**

```python
name = input('Enter your name: ')
age = int(input('Enter your age: ')) # Convert to int
```

---

## 🔄 7. Type Conversion

![Type Conversion](python_study_assets/python_type_conversion_graphic_1769916871842.png)

### Implicit vs Explicit
*   **Implicit**: Python handles it (e.g., `int + float = float`).
*   **Explicit**: User converts it using `int()`, `float()`, `str()`.

```python
s = "100"
n = int(s) # String to Integer
```

---

## 🧱 8. Literals

![Literals](python_study_assets/python_literals_graphic_1769916888299.png)

### Definition
Raw values given in a variable or constant.

*   **Numeric**: `100`, `3.14`
*   **String**: `'Hello'`, `"World"`
*   **Boolean**: `True`, `False`
*   **Special**: `None`

---

## ➕ 9. Operators

*No graphic available*

*   **Arithmetic**: `+`, `-`, `*`, `/`, `%`, `**`, `//`
*   **Assignment**: `=`, `+=`, `-=`
*   **Comparison**: `==`, `!=`, `>`, `<`
*   **Logical**: `and`, `or`, `not`

---

## 🚦 10. Conditional Statements

![Conditionals](python_study_assets/python_conditionals_graphic_1769916907767.png)

### Logic Flow

```python
age = 20

if age >= 18:
    print("Adult")
elif age > 12:
    print("Teenager")
else:
    print("Child")
```

---

## 🔁 11. Loops

![Loops](python_study_assets/python_loops_graphic_1769917882692.png)

### Overview
Loops allow code to be executed repeatedly.

### `while` Loop
Repeats as long as a condition is true.

```python
count = 0
while count < 5:
    print(count)
    count += 1
```

### `for` Loop
Iterates over a sequence.

**Iterating a List:**
```python
fruits = ["apple", "banana"]
for fruit in fruits:
    print(fruit)
```

**Iterating a Dictionary:**
```python
person = {'name': 'Vishnu', 'age': 25}
for key, value in person.items():
    print(key, value)
```

**Using `enumerate()`:**
```python
for index, fruit in enumerate(fruits):
    print(f"{index}: {fruit}")
```

### Real-world Example: E-commerce Display

![E-commerce Loop](python_study_assets/python_ecommerce_loop_graphic_1769917982037.png)

```python
products = [{'name': 'Laptop', 'price': 999}, {'name': 'Phone', 'price': 499}]
for product in products:
    print(f"Item: {product['name']} - ${product['price']}")
```

---

## 🏋️ 12. Exercises

![Exercises](python_study_assets/python_exercises_graphic_1769916922645.png)

### Set 1: Basics
1.  Print your bio using `print()`.
2.  Calculate simple math using operators.

### Set 2: Logic
1.  Write a grade calculator using `if-elif-else`.
2.  Create a loop that prints even numbers from 1 to 20.

---

## 🚀 13. Projects

![Projects](python_study_assets/python_projects_graphic_1769916943116.png)

### Project 1: Calculator
Simple arithmetic operations based on user choice.

### Project 2: Grade Analyzer
Takes 5 subject marks and calculates average/grade.

### Project 3: BMI Calculator
Calculates Body Mass Index from height and weight.

### Project 4: Number Guessing Game 🕵️

![Guessing Game](python_study_assets/python_guessing_game_graphic_1769918381075.png)

**Description**: The computer picks a number (1-100). run infinite loop until you guess it.

```python
import random

print("="*40)
print("     NUMBER GUESSING GAME")
print("="*40)

secret = random.randint(1, 100)
attempts = 0

print("I picked a number (1-100). Guess it!")

while True:
    try:
        guess = int(input(f"Attempt {attempts+1}: "))
        attempts += 1
        
        if guess == secret:
            print(f"🎉 Correct! You won in {attempts} attempts.")
            break
        elif guess < secret:
            print("To Low!")
        else:
            print("Too High!")
    except ValueError:
        print("Please enter a valid number.")
```

---
*End of Complete Python Notes*
