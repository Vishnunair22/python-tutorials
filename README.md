# Python Programming - Complete Study Notes

![Python](https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg)

**Comprehensive reference guide for Python fundamentals**

---

## Table of Contents

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

## 1. Print Function

![Print Function](file:///C:/Users/vishn/.gemini/antigravity/brain/84345dc8-0323-44c2-9bf8-fe7d6fb264ed/python_print_function_graphic_1769916778127.png)

### Overview

The `print()` function outputs data to the standard output device (console/terminal). It converts objects to strings and displays them.

**Syntax:**
```python
print(*objects, sep=' ', end='\n', file=sys.stdout, flush=False)
```

### How It Works

1. Accepts one or more objects as arguments
2. Converts each object to string using `str()`
3. Separates multiple objects using the separator
4. Outputs to the specified file stream
5. Appends the end character/string

### Basic Usage

**Printing strings:**
```python
print('Hello World')
```
**Output:**
```
Hello World
```

**Printing numbers:**
```python
print(3, 2, 4, 5, 6)
```
**Output:**
```
3 2 4 5 6
```

**Printing mixed types:**
```python
print(3, 'Toy World', True)
```
**Output:**
```
3 Toy World True
```

### Parameters

#### sep (Separator)

Defines the string inserted between values. Default is space `' '`.

```python
print('Apple', 'Oranges', 'Grapes', sep='/')
```
**Output:**
```
Apple/Oranges/Grapes
```

#### end (End Character)

Specifies what to print at the end. Default is newline `'\n'`.

```python
print('Hello', end=' ')
print('World')
```
**Output:**
```
Hello World
```

---

## 2. Data Types

![Data Types](file:///C:/Users/vishn/.gemini/antigravity/brain/84345dc8-0323-44c2-9bf8-fe7d6fb264ed/python_data_types_graphic_1769916794933.png)

### Overview

Data types specify the kind of value a variable holds. Python data types:
- **Primitive**: int, float, bool, str
- **Collection**: list, tuple, set, dict

### Primitive Data Types

#### Integer (int)

Whole numbers without decimal points.

```python
x = 1
y = -50
z = 1000000
print(type(x))  # <class 'int'>
```

#### Float

Numbers with decimal points.

```python
a = 1.214
b = 3.14e2  # Scientific: 314.0
print(type(a))  # <class 'float'>
```

#### Boolean (bool)

Truth values: `True` or `False`.

```python
is_valid = True
print(int(True))  # 1
print(int(False)) # 0
```

#### String (str)

Sequence of characters.

```python
name = 'Hello'
message = "World"
print(type(name))  # <class 'str'>
```

### Collection Data Types

#### List

Ordered, mutable collection.

```python
numbers = [1, 2, 3, 4, 5]
mixed = [1, 'apple', True]
```

#### Tuple

Ordered, immutable collection.

```python
coordinates = (10, 20)
single = (1,)  # Note the comma
```

#### Set

Unordered collection of unique elements.

```python
unique = {1, 2, 3, 4, 5}
no_dup = {1, 2, 2, 3}  # Becomes {1, 2, 3}
```

#### Dictionary

Key-value pairs.

```python
person = {'name': 'Vishnu', 'age': 25}
print(person['name'])  # Vishnu
```

---

## 3. Variables

![Variables](file:///C:/Users/vishn/.gemini/antigravity/brain/84345dc8-0323-44c2-9bf8-fe7d6fb264ed/python_variables_graphic_1769916816196.png)

### Definition

Variables are named memory locations storing data values.

```python
name = 'Vishnu'
age = 25
height = 5.9
```

### Dynamic Typing

Python determines types at runtime.

```python
var = 10        # int
var = "Hello"   # Now str
var = [1, 2, 3] # Now list
```

### Multiple Assignment

```python
a, b, c = 10, 20, 30
x = y = z = 5
```

### Naming Rules

✅ **Valid:**
```python
name = "Valid"
_private = 10
user_name = "Valid"
age2 = 25
```

❌ **Invalid:**
```python
2name = "Invalid"      # Cannot start with digit
my-variable = "Invalid" # Hyphen not allowed
class = "Invalid"       # Reserved keyword
```

---

## 4. Keywords and Identifiers

![Keywords](file:///C:/Users/vishn/.gemini/antigravity/brain/84345dc8-0323-44c2-9bf8-fe7d6fb264ed/python_keywords_graphic_1769916832000.png)

### Keywords

Reserved words with predefined meanings.

**Common keywords:**
```
False    True     None     and      or       not
if       elif     else     for      while    break
continue return   def      class    import   from
try      except   finally  raise    with     as
in       is       lambda   pass     yield    del
```

### Identifiers

Names given to variables, functions, classes.

**Rules:**
1. Start with letter or underscore
2. Can contain letters, digits, underscores
3. Case-sensitive
4. Cannot be keywords

### Naming Conventions

- **snake_case**: Variables and functions
- **UPPER_CASE**: Constants
- **PascalCase**: Classes

---

## 5. Indentation

![Indentation](file:///C:/Users/vishn/.gemini/antigravity/brain/84345dc8-0323-44c2-9bf8-fe7d6fb264ed/python_indentation_graphic_1769917624660.png)

### Overview

Indentation refers to the spaces at the beginning of a code line. In other programming languages (like C, Java), indentation is for readability only, but in Python, it is **mandatory** to define blocks of code.

**Syntax:**
```python
if True:
    print("This is indented")
    print("Part of the block")
print("Outside the block")
```

### Rules

1.  Use **4 spaces** per indentation level (preferred).
2.  Do not mix tabs and spaces.
3.  All lines in the same block must have the same indentation.

### Common Errors

**IndentationError:**
```python
if True:
print("Error: Expected an indented block")
```

---

## 6. User Input


![User Input](file:///C:/Users/vishn/.gemini/antigravity/brain/84345dc8-0323-44c2-9bf8-fe7d6fb264ed/python_user_input_graphic_1769916848424.png)

### Overview

The `input()` function reads data from keyboard and returns it as a string.

**Syntax:**
```python
input([prompt])
```

### Basic Usage

```python
name = input('Enter your name: ')
print('Hello,', name)
```

### Important: Always Returns String

```python
a = input('Enter a number: ')  # User: 10
b = input('Enter another: ')    # User: 20
sum = int(a) + int(b)          # Convert to int
print(sum)  # 30
```

---

## 7. Type Conversion

![Type Conversion](file:///C:/Users/vishn/.gemini/antigravity/brain/84345dc8-0323-44c2-9bf8-fe7d6fb264ed/python_type_conversion_graphic_1769916871842.png)

### Implicit Conversion

Python automatically converts types.

```python
result = 4 + 5.5  # int + float
print(result)     # 9.5 (float)
```

### Explicit Conversion

#### To Integer

```python
x = int("10")      # String to int
y = int(3.9)       # Float to int (truncates)
z = int(True)      # Boolean to int (1)
```

#### To Float

```python
a = float("3.14")  # String to float
b = float(5)       # Int to float
```

#### To String

```python
s = str(100)       # Int to string
```

#### To Boolean

```python
bool(1)        # True
bool(0)        # False
bool("hello")  # True
bool("")       # False
```

---

## 8. Literals

![Literals](file:///C:/Users/vishn/.gemini/antigravity/brain/84345dc8-0323-44c2-9bf8-fe7d6fb264ed/python_literals_graphic_1769916888299.png)

### Definition

Literals are raw values assigned to variables. They represent fixed constant values in code.

### Numeric Literals

**Integer:**
```python
decimal = 100
binary = 0b1010      # 10 in decimal
octal = 0o12         # 10 in decimal
hexadecimal = 0xA    # 10 in decimal
```

**Float:**
```python
pi = 3.14
scientific = 3.14e2  # 314.0
```

**Complex:**
```python
c = 3 + 4j
print(c.real)  # 3.0
print(c.imag)  # 4.0
```

### String Literals

```python
single = 'Hello'
double = "World"
multi = '''Multiple
lines'''
```

**Escape sequences:**
```python
newline = "Line 1\nLine 2"
tab = "Name:\tValue"
backslash = "C:\\Path"
```

### Boolean Literals

```python
is_true = True
is_false = False
```

### Special Literals

```python
result = None  # Absence of value
```

---

## 10. Conditional Statements

![Conditionals](file:///C:/Users/vishn/.gemini/antigravity/brain/84345dc8-0323-44c2-9bf8-fe7d6fb264ed/python_conditionals_graphic_1769916907767.png)

### if Statement

```python
age = 18
if age >= 18:
    print("Eligible to vote")
```

### if-else Statement

```python
age = 16
if age >= 18:
    print("Can vote")
else:
    print("Cannot vote")
```

### if-elif-else Statement

```python
marks = 75

if marks >= 90:
    grade = 'A'
elif marks >= 80:
    grade = 'B'
elif marks >= 70:
    grade = 'C'
else:
    grade = 'F'
    
print(f"Grade: {grade}")
```

### Nested if

```python
age = 25
has_license = True

if age >= 18:
    if has_license:
        print("Can drive")
    else:
        print("Need license")
else:
    print("Too young")
```

### Ternary Operator

```python
age = 20
status = "Adult" if age >= 18 else "Minor"
```

---

## 11. Loops

![Loops](file:///C:/Users/vishn/.gemini/antigravity/brain/84345dc8-0323-44c2-9bf8-fe7d6fb264ed/python_loops_graphic_1769917882692.png)

### Overview
Loops allow code to be executed repeatedly based on a condition.

### while Loop
Executes a block of code as long as a condition is true.

```python
count = 0
while count < 5:
    print(count)
    count += 1
```

### for Loop
Iterates over a sequence (like a list, tuple, or string).

**Basic List Iteration:**
```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

**Iterating a String:**
```python
for char in "Python":
    print(char)
# Prints P, y, t, h, o, n on new lines
```

**Iterating a Dictionary:**
```python
person = {'name': 'Vishnu', 'age': 25}

# Iterate keys (default)
for key in person:
    print(key) 

# Iterate values
for value in person.values():
    print(value)

# Iterate key-value pairs
for key, value in person.items():
    print(f"{key}: {value}")
```

**Nested Loops:**
```python
adj = ["red", "tasty"]
fruits = ["apple", "cherry"]

for x in adj:
    for y in fruits:
        print(x, y)
```

**Useful Functions:**

*   `enumerate()`: Returns index and value.
    ```python
    colors = ['red', 'green', 'blue']
    for index, color in enumerate(colors):
        print(f"{index}: {color}")
    ```

*   `zip()`: Iterate over multiple lists simultaneously.
    ```python
    names = ['Alice', 'Bob']
    ages = [25, 30]
    for name, age in zip(names, ages):
        print(f"{name} is {age} years old")
    ```

### range() Function
Generates a sequence of numbers.
`range(start, stop, step)`

```python
for i in range(1, 6):
    print(i) # Prints 1 to 5
```

### Loop Control Statements
*   **break**: Terminates the loop.
*   **continue**: Skips the current iteration.

### Real-world Example: E-commerce Product Display

![E-commerce Loop](file:///C:/Users/vishn/.gemini/antigravity/brain/84345dc8-0323-44c2-9bf8-fe7d6fb264ed/python_ecommerce_loop_graphic_1769917982037.png)

Iterating through a list of products to display them on a webpage.

```python
products = [
    {'name': 'Laptop', 'price': 999},
    {'name': 'Smartphone', 'price': 499},
    {'name': 'Headphones', 'price': 199}
]

print("Available Products:")
for product in products:
    print(f"Product: {product['name']} | Price: ${product['price']}")
    # In a real app, this would create HTML elements like:
    # <div class='card'>...</div>
```

---

## 12. Exercises

![Exercises](file:///C:/Users/vishn/.gemini/antigravity/brain/84345dc8-0323-44c2-9bf8-fe7d6fb264ed/python_exercises_graphic_1769916922645.png)

### Set 1: Print Function

**Exercise 1.1:** Print your details
```python
print("Name: Vishnu")
print("Age: 25")
print("City: Palakkad")
```

**Exercise 1.2:** Custom separator
```python
print('Python', 'Java', 'C++', sep=' | ')
# Output: Python | Java | C++
```

### Set 2: Data Types

**Exercise 2.1:** Create and print variables
```python
name = "Alice"
age = 25
height = 5.6
is_student = True

print(f"{name}, {age}, {height}, {is_student}")
```

**Exercise 2.2:** List operations
```python
fruits = ['apple', 'banana', 'orange']
fruits.append('grape')
fruits.remove('banana')
print(fruits)  # ['apple', 'orange', 'grape']
```

### Set 3: Type Conversion

**Exercise 3.1:** Temperature converter
```python
celsius = float(input("Celsius: "))
fahrenheit = (celsius * 9/5) + 32
print(f"{celsius}°C = {fahrenheit}°F")
```

### Set 4: Operators

**Exercise 4.1:** Calculator
```python
a = 25
b = 4
print(f"{a} + {b} = {a + b}")
print(f"{a} - {b} = {a - b}")
print(f"{a} * {b} = {a * b}")
print(f"{a} / {b} = {a / b}")
```

### Set 5: Conditionals

**Exercise 5.1:** Grade calculator
```python
marks = 87

if marks >= 90:
    print("Grade: A+")
elif marks >= 80:
    print("Grade: A")
elif marks >= 70:
    print("Grade: B")
else:
    print("Grade: C")
```

**Exercise 5.2:** Leap year checker
```python
year = 2024

if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
    print(f"{year} is a leap year")
else:
    print(f"{year} is not a leap year")
```

---

## 13. Projects

![Projects](file:///C:/Users/vishn/.gemini/antigravity/brain/84345dc8-0323-44c2-9bf8-fe7d6fb264ed/python_projects_graphic_1769916943116.png)

### Project 1: Calculator

**Description:** Basic arithmetic calculator

```python
print("=" * 40)
print("       CALCULATOR")
print("=" * 40)

num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))

print("\nOperations:")
print("1. Addition")
print("2. Subtraction")
print("3. Multiplication")
print("4. Division")

choice = input("\nChoice (1-4): ")

if choice == '1':
    result = num1 + num2
    op = "+"
elif choice == '2':
    result = num1 - num2
    op = "-"
elif choice == '3':
    result = num1 * num2
    op = "*"
elif choice == '4':
    if num2 != 0:
        result = num1 / num2
        op = "/"
    else:
        print("Error: Division by zero!")
        exit()
else:
    print("Invalid choice!")
    exit()

print(f"\nResult: {num1} {op} {num2} = {result}")
```

### Project 2: Student Grade Analyzer

**Description:** Calculate and analyze student grades

```python
print("=" * 50)
print("     STUDENT GRADE ANALYZER")
print("=" * 50)

name = input("\nStudent name: ")

print("\nEnter marks (out of 100):")
math = float(input("Mathematics: "))
physics = float(input("Physics: "))
chemistry = float(input("Chemistry: "))
english = float(input("English: "))
computer = float(input("Computer: "))

grades = [math, physics, chemistry, english, computer]
subjects = ['Mathematics', 'Physics', 'Chemistry', 'English', 'Computer']

total = sum(grades)
average = total / len(grades)
maximum = max(grades)
minimum = min(grades)

if average >= 90:
    grade = 'A+'
elif average >= 80:
    grade = 'A'
elif average >= 70:
    grade = 'B'
elif average >= 60:
    grade = 'C'
else:
    grade = 'F'

print("\n" + "=" * 50)
print("           GRADE REPORT")
print("=" * 50)
print(f"\nStudent: {name}")
print("\n" + "-" * 50)

for i in range(len(subjects)):
    print(f"{subjects[i]:<20}: {grades[i]:>6.2f}/100")

print("-" * 50)
print(f"{'Total':<20}: {total:>6.2f}/500")
print(f"{'Average':<20}: {average:>6.2f}%")
print(f"{'Highest':<20}: {maximum:>6.2f}")
print(f"{'Lowest':<20}: {minimum:>6.2f}")
print("-" * 50)
print(f"{'Grade':<20}: {grade}")
print("=" * 50)
```

### Project 3: BMI Calculator

**Description:** Calculate and categorize BMI

```python
print("=" * 40)
print("      BMI CALCULATOR")
print("=" * 40)

name = input("\nEnter your name: ")
weight = float(input("Weight (kg): "))
height = float(input("Height (m): "))

bmi = weight / (height ** 2)

print(f"\n{name}'s BMI: {bmi:.2f}")

if bmi < 18.5:
    category = "Underweight"
    advice = "Consider gaining weight"
elif bmi < 25:
    category = "Normal weight"
    advice = "Maintain current weight"
elif bmi < 30:
    category = "Overweight"
    advice = "Consider losing weight"
else:
    category = "Obese"
    advice = "Consult a healthcare provider"

print(f"Category: {category}")
print(f"Advice: {advice}")
```

### Project 4: Number Guessing Game

![Guessing Game](file:///C:/Users/vishn/.gemini/antigravity/brain/84345dc8-0323-44c2-9bf8-fe7d6fb264ed/python_guessing_game_graphic_1769918381075.png)

**Description:** Guess a random number between 1 and 100. Keep guessing until you get it right!

```python
import random

print("=" * 40)
print("     NUMBER GUESSING GAME")
print("=" * 40)

secret_number = random.randint(1, 100)
attempts = 0

print("\nI have chosen a number between 1 and 100.")
print("Can you guess it?\\n")

while True:
    guess = int(input(f"Attempt {attempts + 1}: Enter your guess: "))
    attempts += 1

    if guess == secret_number:
        print(f"\\n🎉 Congratulations! You guessed the number in {attempts} attempts!")
        break
    elif guess < secret_number:
        print("Too low! Try again.")
    else:
        print("Too high! Try again.")
```

---

*End of Study Notes*
