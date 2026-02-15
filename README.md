# Python Tutorial Notes

A comprehensive guide covering fundamental Python concepts with examples and exercises.

---

## Table of Contents
1. [Printing Statements](#printing-statements)
2. [Data Types](#data-types)
3. [Comments](#comments)
4. [Variables](#variables)
5. [Keywords and Identifiers](#keywords-and-identifiers)
6. [User Input](#user-input)
7. [Type Conversion](#type-conversion)
8. [Literals](#literals)
9. [Operators](#operators)
10. [Control Flow - If/Else Statements](#control-flow---ifelse-statements)
11. [Loops](#loops)

---

## Printing Statements

In Python, we use the `print()` function to display output. You can print any data type using this function.

### Syntax
```python
print(value1, value2, ..., sep=' ', end='\n')
```

**Parameters:**
- `args`: The values to be printed
- `sep`: Separator between values (default is a space `' '`)
- `end`: What should be at the end of the output (default is a newline `\n`)

### Printing Different Data Types

#### Integers
```python
print(42, 22, 32)
# Output: 42 22 32
```

#### Floating Point Numbers
```python
print(2.21, 32.12, 12.4)
# Output: 2.21 32.12 12.4
```

#### Boolean Values
```python
print(True)   # Output: True
print(False)  # Output: False
```

#### Strings
Strings can be enclosed in single quotes `''`, double quotes `""`, or triple quotes `'''` for multi-line strings.

```python
print('Ajay', 'Athul', 'Sam')
# Output: Ajay Athul Sam

print("This is a sentence I want to print")
# Output: This is a sentence I want to print

print('''This is a paragraph I want to print.
It is quite long so it spans multiple lines''')
```

### Practice Exercises

**Exercise 1:** Print your name, age, and city on the same line.
```python
# Solution:
print("John", 25, "New York")
```

**Exercise 2:** Print three numbers separated by a hyphen instead of a space.
```python
# Solution:
print(10, 20, 30, sep='-')
# Output: 10-20-30
```

**Exercise 3:** Print two sentences on the same line without a line break between them.
```python
# Solution:
print("Hello", end=' ')
print("World")
# Output: Hello World
```

---

## Data Types

Python has three main categories of data types: **Basic**, **Container**, and **User Defined**.

### Basic Data Types

#### 1. Integer
Contains whole numbers like 1, 2, 4, 100. The highest possible number is approximately 1e309.

```python
x = 42
y = -15
z = 1000
```

#### 2. Floating Point
Contains decimal numbers. The largest possible number is approximately 1.7e308.

```python
pi = 3.14159
temperature = -12.5
large_num = 1.5e10  # Scientific notation
```

#### 3. Boolean
Contains logical values `True` or `False`, which are generally results of logical operations.

```python
is_valid = True
is_complete = False
```

**Note:** Python treats `True` as 1 and `False` as 0.

#### 4. Complex
Python supports complex numbers with real and imaginary parts.

```python
complex_num = 1 + 6j
```

#### 5. String
Strings are sequences of characters - letters, words, and sentences.

```python
name = 'Vishnu'
sentence = "This is a string"
paragraph = '''This is a multi-line
string that can span
multiple lines'''
```

### Container Data Types

#### 1. Lists
Used to store a collection of items. Lists are **mutable** (can be changed) and ordered.

```python
Fruits = ['Apple', 'Oranges', 'Bananas']
numbers = [1, 2, 3, 4, 5]
mixed = [1, 'hello', 3.14, True]
```

#### 2. Tuples
Similar to lists but **immutable** (cannot be changed after creation). Use parentheses `()`.

```python
Hobbies = ('Driving', 'Cricket', 'Hockey')
coordinates = (10, 20)
```

#### 3. Sets
Unordered collection of unique items. Similar to mathematical sets. Use curly braces `{}`.

```python
Numbers = {1, 2, 3, 5, 6}
unique_letters = {'a', 'b', 'c'}
```

#### 4. Dictionaries
Store data in key-value pairs. Very useful for structured data.

```python
Class = {'Name': 'Eleventh', 'Batch': 'C', 'Students': 50}
Student = {'Name': 'Vishnu', 'Age': 25}
```

### User Defined Data Types
- **Classes**: User-defined blueprints for creating objects
- **Objects**: Instances of classes

### Practice Exercises

**Exercise 4:** Create a list of 5 programming languages you know or want to learn.
```python
# Solution:
languages = ['Python', 'JavaScript', 'Java', 'C++', 'Ruby']
print(languages)
```

**Exercise 5:** Create a dictionary representing a book with keys: title, author, and year.
```python
# Solution:
book = {'title': 'Python Programming', 'author': 'John Doe', 'year': 2023}
print(book)
```

**Exercise 6:** Create a tuple of your favorite three colors.
```python
# Solution:
colors = ('Blue', 'Green', 'Purple')
print(colors)
```

---

## Comments

Comments are pieces of code that are not executed by the compiler. They are used to:
- Explain code for easier understanding
- Provide documentation
- Make code more maintainable
- Serve as reference for future development

### Syntax
In Python, we use `#` for single-line comments.

```python
# This is a comment
# This is also a comment

x = 5  # This comment is at the end of a line
```

### Multi-line Comments
For multi-line comments, use triple quotes (though technically these are strings).

```python
'''
This is a multi-line comment.
It can span several lines.
Useful for longer explanations.
'''
```

### Practice Exercises

**Exercise 7:** Add comments to explain the following code:
```python
# Solution:
# Calculate the area of a rectangle
length = 10  # Length in meters
width = 5    # Width in meters
area = length * width  # Area formula: length × width
print(area)  # Display the result
```

---

## Variables

Variables are containers that store values for use in a program. They act as placeholders for data that may change during program execution.

### Key Features
- **Dynamic Typing**: No need to declare variable type
- **Dynamic Binding**: Can easily reassign variable values

### Variable Declaration

```python
name = 'Sam'
age = 25
height = 5.9
is_student = True
```

### Multiple Variables in a Single Line

```python
a = 5; b = 6; c = 7
print(a)  # Output: 5
print(b)  # Output: 6
print(c)  # Output: 7
```

Or using unpacking:
```python
x, y, z = 10, 20, 30
```

### Variable Naming Rules
1. Can contain letters, numbers, and underscores
2. Must start with a letter or underscore
3. Case-sensitive (`name` and `Name` are different)
4. Cannot use Python keywords
5. Use descriptive names

### Practice Exercises

**Exercise 8:** Create variables for a student's information (name, roll number, grade, marks).
```python
# Solution:
student_name = 'Ajay'
roll_number = 101
grade = 'A'
marks = 95.5
print(student_name, roll_number, grade, marks)
```

**Exercise 9:** Swap the values of two variables.
```python
# Solution:
x = 10
y = 20
x, y = y, x  # Swapping
print(x, y)  # Output: 20 10
```

**Exercise 10:** Create variables for the dimensions of a room and calculate its area.
```python
# Solution:
room_length = 15
room_width = 12
room_area = room_length * room_width
print("Room area:", room_area, "square meters")
```

---

## Keywords and Identifiers

### Keywords
Special reserved words in Python that have predefined meanings. They cannot be used as variable names.

**Examples:** `print`, `input`, `if`, `else`, `for`, `while`, `def`, `class`, `return`, `True`, `False`, `None`

Keywords help the compiler convert high-level code to machine code efficiently.

```python
# Valid
my_print = 5

# Invalid - 'print' is a keyword
# print = 5  # This will cause an error
```

### Identifiers
Names used to identify variables, functions, classes, or other objects.

**Rules for Identifiers:**
1. Can contain letters (a-z, A-Z), digits (0-9), and underscores (_)
2. Must start with a letter or underscore
3. Cannot start with a digit
4. Case-sensitive
5. Cannot be a Python keyword
6. No special characters allowed

```python
# Valid identifiers
student_name = "John"
_private_var = 42
user1 = "Alice"
myVariable = 100

# Invalid identifiers
# 1st_variable = 5  # Cannot start with digit
# my-variable = 10  # Hyphen not allowed
# for = 20          # Keyword cannot be used
```

### Practice Exercises

**Exercise 11:** Identify which of the following are valid variable names:
- `user_age` ✓ Valid
- `2nd_place` ✗ Invalid (starts with digit)
- `_temp` ✓ Valid
- `my-value` ✗ Invalid (hyphen not allowed)
- `class` ✗ Invalid (keyword)
- `user1` ✓ Valid

---

## User Input

Software applications can be categorized as:
- **Static Software**: Programs with fixed output (e.g., Calendar, Clock)
- **Dynamic Software**: Programs that respond to user input (e.g., YouTube, Social Media apps)

### The input() Function
In Python, we use `input()` to accept data from users. The function always returns a **string**.

```python
name = input("Enter your name: ")
print("Hello,", name)
```

### Reading Different Data Types
Since `input()` returns a string, you need to convert it to the appropriate type.

```python
# Reading an integer
age = int(input("Enter your age: "))

# Reading a float
height = float(input("Enter your height in meters: "))

# Reading multiple values
x, y = input("Enter two numbers: ").split()
```

### Practice Exercises

**Exercise 12:** Write a program to accept a user's name and greet them.
```python
# Solution:
name = input("What is your name? ")
print("Hello, " + name + "! Welcome to Python programming.")
```

**Exercise 13:** Write a program to calculate the area of a rectangle using user input.
```python
# Solution:
length = float(input("Enter the length: "))
width = float(input("Enter the width: "))
area = length * width
print("The area of the rectangle is:", area)
```

**Exercise 14:** Create a program that asks for three numbers and prints their sum.
```python
# Solution:
num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))
num3 = float(input("Enter third number: "))
total = num1 + num2 + num3
print("The sum is:", total)
```

---

## Type Conversion

Type conversion is the process of converting one data type to another. Python supports two types of conversion:

### 1. Implicit Type Conversion
Python automatically converts data types when needed.

```python
x = 10      # integer
y = 5.5     # float
result = x + y  # x is automatically converted to float
print(result)   # Output: 15.5
print(type(result))  # Output: <class 'float'>
```

### 2. Explicit Type Conversion
The programmer manually converts data types using built-in functions.

#### Common Conversion Functions

**int()** - Convert to integer
```python
x = int(5.9)        # 5
y = int("100")      # 100
```

**float()** - Convert to float
```python
x = float(5)        # 5.0
y = float("3.14")   # 3.14
```

**str()** - Convert to string
```python
x = str(100)        # "100"
y = str(3.14)       # "3.14"
```

**bool()** - Convert to boolean
```python
x = bool(1)         # True
y = bool(0)         # False
z = bool("")        # False
w = bool("hello")   # True
```

### Finding Data Type
Use the `type()` function to find the data type of any value or variable.

```python
x = 42
print(type(x))  # Output: <class 'int'>

y = "Hello"
print(type(y))  # Output: <class 'str'>
```

### Practice Exercises

**Exercise 15:** Convert a string to an integer and perform arithmetic.
```python
# Solution:
num_str = "50"
num_int = int(num_str)
result = num_int + 25
print("Result:", result)  # Output: Result: 75
```

**Exercise 16:** Take two numbers as input and display their sum (handle type conversion).
```python
# Solution:
num1 = input("Enter first number: ")
num2 = input("Enter second number: ")
sum_result = float(num1) + float(num2)
print("Sum:", sum_result)
```

**Exercise 17:** Check the type of different values.
```python
# Solution:
print(type(100))           # <class 'int'>
print(type(3.14))          # <class 'float'>
print(type("Python"))      # <class 'str'>
print(type(True))          # <class 'bool'>
print(type([1, 2, 3]))     # <class 'list'>
```

---

## Literals

Literals are raw data assigned to variables. They represent fixed values in the code.

### Types of Literals

#### 1. Numeric Literals

**Integer Literals**
```python
decimal = 100           # Decimal
binary = 0b1010        # Binary (equals 10 in decimal)
octal = 0o12           # Octal (equals 10 in decimal)
hexadecimal = 0xA      # Hexadecimal (equals 10 in decimal)
```

**Floating Point Literals**
```python
simple = 3.14
scientific = 1.5e2     # 1.5 × 10² = 150.0
```

**Complex Literals**
```python
complex_num = 3 + 4j
```

#### 2. String Literals

**Single-line Strings**
```python
single = 'Hello'
double = "World"
```

**Multi-line Strings**
```python
multi = '''This is
a multi-line
string'''
```

**Unicode Strings**
```python
unicode_str = u"Hello \u00e9"  # Hello é
```

**Raw Strings** (backslashes are treated literally)
```python
raw = r"C:\Users\name\folder"  # Backslashes not escaped
```

#### 3. Boolean Literals
```python
is_active = True   # Treated as 1
is_deleted = False # Treated as 0
```

#### 4. Special Literals
**None** - Represents the absence of a value
```python
result = None
```

### Practice Exercises

**Exercise 18:** Create variables with different numeric literal formats representing the number 16.
```python
# Solution:
decimal = 16
binary = 0b10000
octal = 0o20
hexadecimal = 0x10

print(decimal, binary, octal, hexadecimal)
# Output: 16 16 16 16
```

**Exercise 19:** Use a raw string to represent a file path.
```python
# Solution:
file_path = r"C:\Users\Documents\python_files\script.py"
print(file_path)
```

**Exercise 20:** Create a variable with None and check its type.
```python
# Solution:
empty_value = None
print(empty_value)      # Output: None
print(type(empty_value))  # Output: <class 'NoneType'>
```

---

## Operators

Operators are special symbols that perform operations on variables and values. Python supports various types of operators for different purposes.

### 1. Arithmetic Operators

Arithmetic operators are used to perform mathematical operations.

| Operator | Name | Example | Result |
|----------|------|---------|--------|
| + | Addition | 5 + 3 | 8 |
| - | Subtraction | 5 - 3 | 2 |
| * | Multiplication | 5 * 3 | 15 |
| / | Division | 5 / 2 | 2.5 |
| // | Floor Division | 5 // 2 | 2 |
| % | Modulus (Remainder) | 5 % 2 | 1 |
| ** | Exponentiation | 5 ** 2 | 25 |

#### Examples

```python
# Basic arithmetic
a = 10
b = 3

print(a + b)   # Output: 13
print(a - b)   # Output: 7
print(a * b)   # Output: 30
print(a / b)   # Output: 3.333...
print(a // b)  # Output: 3 (floor division)
print(a % b)   # Output: 1 (remainder)
print(a ** b)  # Output: 1000 (10 cubed)

# Practical examples
total_cost = 100 + 50 + 75
print("Total:", total_cost)  # Output: Total: 225

# Calculate average
num1, num2, num3 = 85, 90, 78
average = (num1 + num2 + num3) / 3
print("Average:", average)  # Output: Average: 84.33...
```

### 2. Comparison Operators

Comparison operators compare two values and return a Boolean result (`True` or `False`).

| Operator | Name | Example | Result |
|----------|------|---------|--------|
| == | Equal to | 5 == 5 | True |
| != | Not equal to | 5 != 3 | True |
| > | Greater than | 5 > 3 | True |
| < | Less than | 5 < 3 | False |
| >= | Greater than or equal to | 5 >= 5 | True |
| <= | Less than or equal to | 5 <= 3 | False |

#### Examples

```python
x = 10
y = 20

print(x == y)   # Output: False
print(x != y)   # Output: True
print(x > y)    # Output: False
print(x < y)    # Output: True
print(x >= 10)  # Output: True
print(y <= 15)  # Output: False

# Comparing strings
name1 = "Alice"
name2 = "Bob"
print(name1 == name2)  # Output: False
print(name1 != name2)  # Output: True
```

### 3. Logical Operators

Logical operators are used to combine conditional statements.

| Operator | Description | Example | Result |
|----------|-------------|---------|--------|
| and | Returns True if both statements are true | True and True | True |
| or | Returns True if at least one statement is true | True or False | True |
| not | Reverses the result | not True | False |

#### Examples

```python
# and operator
age = 25
has_license = True
print(age >= 18 and has_license)  # Output: True

# or operator
is_weekend = False
is_holiday = True
print(is_weekend or is_holiday)  # Output: True

# not operator
is_raining = False
print(not is_raining)  # Output: True

# Complex conditions
score = 85
attendance = 90
print(score >= 80 and attendance >= 75)  # Output: True
print(score >= 90 or attendance >= 85)   # Output: True
print(not (score < 50))                   # Output: True
```

### 4. Assignment Operators

Assignment operators are used to assign values to variables.

| Operator | Example | Equivalent to |
|----------|---------|---------------|
| = | x = 5 | x = 5 |
| += | x += 3 | x = x + 3 |
| -= | x -= 3 | x = x - 3 |
| *= | x *= 3 | x = x * 3 |
| /= | x /= 3 | x = x / 3 |
| //= | x //= 3 | x = x // 3 |
| %= | x %= 3 | x = x % 3 |
| **= | x **= 3 | x = x ** 3 |

#### Examples

```python
# Simple assignment
x = 10
print(x)  # Output: 10

# Addition assignment
x += 5  # Same as x = x + 5
print(x)  # Output: 15

# Subtraction assignment
x -= 3  # Same as x = x - 3
print(x)  # Output: 12

# Multiplication assignment
x *= 2  # Same as x = x * 2
print(x)  # Output: 24

# Division assignment
x /= 4  # Same as x = x / 4
print(x)  # Output: 6.0

# Modulus assignment
score = 100
score %= 30  # Same as score = score % 30
print(score)  # Output: 10

# Exponentiation assignment
base = 2
base **= 3  # Same as base = base ** 3
print(base)  # Output: 8
```

### 5. Bitwise Operators

Bitwise operators work on bits and perform bit-by-bit operations.

| Operator | Name | Description | Example |
|----------|------|-------------|---------|
| & | AND | Sets each bit to 1 if both bits are 1 | 5 & 3 = 1 |
| \| | OR | Sets each bit to 1 if one of the bits is 1 | 5 \| 3 = 7 |
| ^ | XOR | Sets each bit to 1 if only one bit is 1 | 5 ^ 3 = 6 |
| ~ | NOT | Inverts all the bits | ~5 = -6 |
| << | Left Shift | Shifts left by pushing zeros from right | 5 << 1 = 10 |
| >> | Right Shift | Shifts right by pushing copies from left | 5 >> 1 = 2 |

#### Examples

```python
a = 5   # Binary: 0101
b = 3   # Binary: 0011

print(a & b)   # Output: 1  (Binary: 0001)
print(a | b)   # Output: 7  (Binary: 0111)
print(a ^ b)   # Output: 6  (Binary: 0110)
print(~a)      # Output: -6
print(a << 1)  # Output: 10 (Binary: 1010)
print(a >> 1)  # Output: 2  (Binary: 0010)
```

### 6. Membership Operators

Membership operators test whether a value is present in a sequence (list, tuple, string, etc.).

| Operator | Description | Example |
|----------|-------------|---------|
| in | Returns True if value is in sequence | 'a' in 'apple' |
| not in | Returns True if value is not in sequence | 'z' not in 'apple' |

#### Examples

```python
# String membership
text = "Hello World"
print('H' in text)        # Output: True
print('x' in text)        # Output: False
print('Python' not in text)  # Output: True

# List membership
fruits = ['apple', 'banana', 'orange']
print('apple' in fruits)     # Output: True
print('grape' in fruits)     # Output: False
print('mango' not in fruits) # Output: True

# Tuple membership
numbers = (1, 2, 3, 4, 5)
print(3 in numbers)      # Output: True
print(10 not in numbers) # Output: True

# Dictionary membership (checks keys)
student = {'name': 'John', 'age': 20}
print('name' in student)    # Output: True
print('grade' in student)   # Output: False
```

### 7. Identity Operators

Identity operators compare the memory locations of two objects.

| Operator | Description | Example |
|----------|-------------|---------|
| is | Returns True if both variables are the same object | x is y |
| is not | Returns True if both variables are not the same object | x is not y |

#### Examples

```python
# Identity with numbers
x = 5
y = 5
z = 10

print(x is y)      # Output: True (same object in memory)
print(x is z)      # Output: False
print(x is not z)  # Output: True

# Identity with lists
list1 = [1, 2, 3]
list2 = [1, 2, 3]
list3 = list1

print(list1 == list2)    # Output: True (same values)
print(list1 is list2)    # Output: False (different objects)
print(list1 is list3)    # Output: True (same object)

# Identity with None
value = None
print(value is None)     # Output: True
print(value is not None) # Output: False
```

### 8. Operator Precedence

Operators are executed in a specific order. Here's the precedence from highest to lowest:

1. `**` (Exponentiation)
2. `~`, `+`, `-` (Unary operators)
3. `*`, `/`, `//`, `%` (Multiplication, Division, Floor Division, Modulus)
4. `+`, `-` (Addition, Subtraction)
5. `<<`, `>>` (Bitwise shifts)
6. `&` (Bitwise AND)
7. `^` (Bitwise XOR)
8. `|` (Bitwise OR)
9. `==`, `!=`, `>`, `<`, `>=`, `<=`, `is`, `is not`, `in`, `not in` (Comparisons)
10. `not` (Logical NOT)
11. `and` (Logical AND)
12. `or` (Logical OR)

#### Examples

```python
# Precedence example
result = 2 + 3 * 4
print(result)  # Output: 14 (not 20, because * has higher precedence)

# Using parentheses to change order
result = (2 + 3) * 4
print(result)  # Output: 20

# Complex expression
result = 10 + 5 * 2 ** 2
print(result)  # Output: 30 (2**2 = 4, then 5*4 = 20, then 10+20 = 30)
```

### Practice Exercises

**Exercise 21:** Calculate the total price of 3 items costing $25.50, $15.75, and $30.25.
```python
# Solution:
item1 = 25.50
item2 = 15.75
item3 = 30.25
total = item1 + item2 + item3
print("Total price: $", total)  # Output: Total price: $ 71.5
```

**Exercise 22:** Check if a number is even or odd using the modulus operator.
```python
# Solution:
number = int(input("Enter a number: "))
if number % 2 == 0:
    print(number, "is even")
else:
    print(number, "is odd")
```

**Exercise 23:** Calculate compound interest using the formula: A = P(1 + r/n)^(nt)
```python
# Solution:
principal = 1000  # Initial amount
rate = 0.05       # 5% annual rate
time = 2          # 2 years
n = 4             # Compounded quarterly

amount = principal * (1 + rate/n) ** (n * time)
interest = amount - principal
print("Final amount:", round(amount, 2))
print("Interest earned:", round(interest, 2))
```

**Exercise 24:** Use comparison operators to check if someone is eligible to vote (age >= 18).
```python
# Solution:
age = int(input("Enter your age: "))
is_eligible = age >= 18
print("Eligible to vote:", is_eligible)
```

**Exercise 25:** Use logical operators to check if a year is a leap year.
```python
# Solution:
# A leap year is divisible by 4, but not by 100 unless also divisible by 400
year = int(input("Enter a year: "))
is_leap = (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0)
print(year, "is a leap year:", is_leap)
```

**Exercise 26:** Use augmented assignment operators to calculate the total after applying discount.
```python
# Solution:
price = 500
discount_percent = 20

# Calculate discount amount
discount = price * discount_percent / 100
price -= discount  # Same as price = price - discount

print("Final price after discount: $", price)  # Output: $ 400.0
```

**Exercise 27:** Check if a character is a vowel using membership operator.
```python
# Solution:
vowels = 'aeiouAEIOU'
char = input("Enter a character: ")
if char in vowels:
    print(char, "is a vowel")
else:
    print(char, "is not a vowel")
```

**Exercise 28:** Use bitwise operators to swap two numbers without using a temporary variable.
```python
# Solution:
a = 10
b = 20
print("Before swap: a =", a, ", b =", b)

a = a ^ b
b = a ^ b
a = a ^ b

print("After swap: a =", a, ", b =", b)
# Output: After swap: a = 20 , b = 10
```

**Exercise 29:** Calculate the power of a number using the exponentiation operator.
```python
# Solution:
base = int(input("Enter base: "))
exponent = int(input("Enter exponent: "))
result = base ** exponent
print(base, "raised to the power", exponent, "=", result)
```

**Exercise 30:** Demonstrate operator precedence with a complex expression.
```python
# Solution:
# Calculate: (10 + 5) * 2 - 3 ** 2
result1 = (10 + 5) * 2 - 3 ** 2
print("With parentheses:", result1)  # Output: 21

# Without proper parentheses
result2 = 10 + 5 * 2 - 3 ** 2
print("Without parentheses:", result2)  # Output: 11

# Explanation:
# result1: (10 + 5) = 15, then 15 * 2 = 30, 3 ** 2 = 9, 30 - 9 = 21
# result2: 3 ** 2 = 9, 5 * 2 = 10, 10 + 10 = 20, 20 - 9 = 11
```

---

## Control Flow - If/Else Statements

Programs typically execute from top to bottom, line by line. However, we often need **branching** - the ability to execute different code based on conditions. This is where control flow statements come in.

**Real-world example:** Consider a login system where users enter credentials. The program checks if they're valid - if yes, the user is authenticated; if no, access is denied.

### Basic If Statement

The `if` statement executes a block of code only when a condition is true.

#### Syntax
```python
if condition:
    statement1
    statement2
```

#### Examples

```python
# Simple if statement
age = 20
if age >= 18:
    print("You are an adult")

# Multiple statements
temperature = 35
if temperature > 30:
    print("It's hot outside!")
    print("Stay hydrated")

# Using comparison operators
score = 85
if score >= 80:
    print("Excellent performance!")
```

### If-Else Statement

The `else` clause executes when the `if` condition is false.

#### Syntax
```python
if condition:
    statement1
else:
    statement2
```

#### Examples

```python
# Basic if-else
age = 15
if age >= 18:
    print("You can vote")
else:
    print("You cannot vote yet")

# Login example
user_email = input('Enter your email: ')
user_password = input('Enter your password: ')

if user_email == 'user@gmail.com' and user_password == '1234':
    print('Welcome! Login successful.')
else:
    print('Sorry, incorrect username or password')

# Number check
number = int(input("Enter a number: "))
if number % 2 == 0:
    print(number, "is even")
else:
    print(number, "is odd")
```

### Elif Statement

When you have multiple conditions to check, use `elif` (else if). Python checks conditions from top to bottom and executes the first true condition.

#### Syntax
```python
if condition1:
    statement1
elif condition2:
    statement2
elif condition3:
    statement3
else:
    statement4
```

#### Examples

```python
# Grade calculator
marks = int(input("Enter your marks: "))

if marks >= 90:
    print("Grade: A+")
elif marks >= 80:
    print("Grade: A")
elif marks >= 70:
    print("Grade: B")
elif marks >= 60:
    print("Grade: C")
elif marks >= 50:
    print("Grade: D")
else:
    print("Grade: F - Failed")

# Traffic light system
signal = input("Enter signal color (red/yellow/green): ").lower()

if signal == 'red':
    print("STOP!")
elif signal == 'yellow':
    print("Get Ready")
elif signal == 'green':
    print("GO!")
else:
    print("Invalid signal color")

# Age category
age = 25
if age < 13:
    print("Child")
elif age < 20:
    print("Teenager")
elif age < 60:
    print("Adult")
else:
    print("Senior")
```

### Nested If Statements

You can place `if` statements inside other `if` statements. This is called nesting.

#### Examples

```python
# Nested if for login with role check
username = "admin"
password = "1234"
role = "admin"

if username == "admin" and password == "1234":
    print("Login successful")
    if role == "admin":
        print("Welcome Admin! You have full access.")
    else:
        print("Welcome User! You have limited access.")
else:
    print("Invalid credentials")

# Age and license check
age = 20
has_license = True

if age >= 18:
    print("You meet the age requirement")
    if has_license:
        print("You can drive!")
    else:
        print("You need to get a license first")
else:
    print("You are too young to drive")

# Number classification
num = int(input("Enter a number: "))

if num > 0:
    print("Positive number")
    if num % 2 == 0:
        print("Even positive number")
    else:
        print("Odd positive number")
elif num < 0:
    print("Negative number")
    if num % 2 == 0:
        print("Even negative number")
    else:
        print("Odd negative number")
else:
    print("Zero")
```

### Indentation in Python

**IMPORTANT:** Python uses **indentation (spaces)** instead of curly braces `{}` to define code blocks. This makes code more readable.

**Rules:**
- Use 4 spaces for each indentation level (recommended)
- Be consistent - don't mix tabs and spaces
- All statements in a block must have the same indentation

```python
# Correct indentation
if True:
    print("This is indented")
    print("This is also indented")
print("This is not indented")

# Incorrect - will cause IndentationError
# if True:
# print("Error - not indented")
#   print("Error - inconsistent indentation")
```

### Ternary Operator (One-Line If-Else)

Python supports a compact way to write simple if-else statements in one line.

#### Syntax
```python
value_if_true if condition else value_if_false
```

#### Examples

```python
# Basic ternary
age = 20
status = "Adult" if age >= 18 else "Minor"
print(status)  # Output: Adult

# With variables
a = 10
b = 20
max_value = a if a > b else b
print("Maximum:", max_value)  # Output: Maximum: 20

# Direct in print
number = 7
print("Even" if number % 2 == 0 else "Odd")  # Output: Odd
```

### Practice Exercises

**Exercise 31:** Write a program to check if a number is positive, negative, or zero.
```python
# Solution:
num = float(input("Enter a number: "))

if num > 0:
    print("Positive number")
elif num < 0:
    print("Negative number")
else:
    print("Zero")
```

**Exercise 32:** Create a simple calculator that performs addition, subtraction, multiplication, or division based on user choice.
```python
# Solution:
num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))
operation = input("Enter operation (+, -, *, /): ")

if operation == '+':
    result = num1 + num2
    print("Result:", result)
elif operation == '-':
    result = num1 - num2
    print("Result:", result)
elif operation == '*':
    result = num1 * num2
    print("Result:", result)
elif operation == '/':
    if num2 != 0:
        result = num1 / num2
        print("Result:", result)
    else:
        print("Error: Cannot divide by zero")
else:
    print("Invalid operation")
```

**Exercise 33:** Write a program to determine if a person is eligible for a discount. Give 20% discount if age < 12 or age > 60, otherwise 10%.
```python
# Solution:
age = int(input("Enter your age: "))
total_price = float(input("Enter total price: "))

if age < 12 or age > 60:
    discount = total_price * 0.20
    print("You get 20% discount!")
else:
    discount = total_price * 0.10
    print("You get 10% discount!")

final_price = total_price - discount
print("Discount amount:", discount)
print("Final price:", final_price)
```

**Exercise 34:** Write a program to check if a year is a leap year using nested if.
```python
# Solution:
year = int(input("Enter a year: "))

if year % 4 == 0:
    if year % 100 == 0:
        if year % 400 == 0:
            print(year, "is a leap year")
        else:
            print(year, "is not a leap year")
    else:
        print(year, "is a leap year")
else:
    print(year, "is not a leap year")
```

**Exercise 35:** Create a program that categorizes BMI (Body Mass Index). BMI < 18.5: Underweight, 18.5-24.9: Normal, 25-29.9: Overweight, >= 30: Obese.
```python
# Solution:
weight = float(input("Enter weight in kg: "))
height = float(input("Enter height in meters: "))

bmi = weight / (height ** 2)
print("Your BMI is:", round(bmi, 2))

if bmi < 18.5:
    print("Category: Underweight")
elif bmi < 25:
    print("Category: Normal weight")
elif bmi < 30:
    print("Category: Overweight")
else:
    print("Category: Obese")
```

---

## Loops

Loops are **iteration control statements** that repeat a block of code multiple times. They are essential when you need to perform repetitive tasks.

**Real-world example:** On an e-commerce site like Flipkart, when you search for a product, many items appear. Instead of manually coding each product container, loops display different products using the same structure.

### Types of Loops in Python
1. **For Loop** - Iterates over a sequence
2. **While Loop** - Repeats while a condition is true

**Note:** Python does not have a traditional do-while loop, but we can achieve similar behavior.

### For Loop

The `for` loop iterates over a sequence (list, tuple, string, range, etc.) and executes code for each item.

#### Syntax
```python
for variable in sequence:
    statement1
    statement2
```

#### Using range() Function

The `range()` function generates a sequence of numbers.

```python
# range(stop) - from 0 to stop-1
range(5)        # 0, 1, 2, 3, 4

# range(start, stop) - from start to stop-1
range(2, 8)     # 2, 3, 4, 5, 6, 7

# range(start, stop, step) - with custom increment
range(0, 10, 2) # 0, 2, 4, 6, 8
range(10, 0, -1) # 10, 9, 8, 7, 6, 5, 4, 3, 2, 1
```

#### Examples

```python
# Basic for loop with range
for i in range(5):
    print(i)
# Output: 0 1 2 3 4

# Loop with start and stop
for i in range(1, 6):
    print("Number:", i)
# Output: Number: 1, Number: 2, ..., Number: 5

# Loop with step
for i in range(0, 11, 2):
    print(i)
# Output: 0 2 4 6 8 10

# Iterating over a list
fruits = ['apple', 'banana', 'orange', 'mango']
for fruit in fruits:
    print("I like", fruit)

# Iterating over a string
for letter in "Python":
    print(letter)
# Output: P y t h o n (each on new line)

# Iterating over a dictionary
student = {'name': 'John', 'age': 20, 'grade': 'A'}
for key in student:
    print(key, ":", student[key])

# Using items() for key-value pairs
for key, value in student.items():
    print(f"{key}: {value}")

# Multiplication table
num = 5
for i in range(1, 11):
    print(f"{num} x {i} = {num * i}")
```

#### Nested For Loops

```python
# Pattern printing
for i in range(1, 5):
    for j in range(i):
        print("*", end=" ")
    print()
# Output:
# * 
# * * 
# * * * 
# * * * * 

# Multiplication table (1-10)
for i in range(1, 11):
    for j in range(1, 11):
        print(f"{i*j:4}", end=" ")
    print()
```

### While Loop

The `while` loop repeats as long as a condition is true. Be careful to avoid infinite loops!

#### Syntax
```python
while condition:
    statement1
    statement2
    # Don't forget to update the condition!
```

#### Examples

```python
# Basic while loop
count = 1
while count <= 5:
    print("Count:", count)
    count += 1
# Output: Count: 1, Count: 2, ..., Count: 5

# Sum of numbers
total = 0
num = 1
while num <= 10:
    total += num
    num += 1
print("Sum:", total)  # Output: Sum: 55

# User input validation
password = ""
while password != "secret":
    password = input("Enter password: ")
    if password != "secret":
        print("Incorrect! Try again.")
print("Access granted!")

# Countdown
n = 5
while n > 0:
    print(n)
    n -= 1
print("Blast off!")
```

#### Infinite Loops (Use with caution!)

```python
# Infinite loop - runs forever unless broken
# while True:
#     print("This runs forever!")

# Practical use with break
while True:
    user_input = input("Enter 'quit' to exit: ")
    if user_input == 'quit':
        break
    print("You entered:", user_input)
```

### Loop Control Statements

#### 1. break - Exit the loop immediately

```python
# Break example
for i in range(1, 11):
    if i == 5:
        break
    print(i)
# Output: 1 2 3 4 (stops at 5)

# Finding first even number
numbers = [1, 3, 5, 8, 9, 10]
for num in numbers:
    if num % 2 == 0:
        print("First even number:", num)
        break
```

#### 2. continue - Skip to the next iteration

```python
# Continue example
for i in range(1, 6):
    if i == 3:
        continue
    print(i)
# Output: 1 2 4 5 (skips 3)

# Print only odd numbers
for i in range(1, 11):
    if i % 2 == 0:
        continue
    print(i)
# Output: 1 3 5 7 9
```

#### 3. pass - Do nothing (placeholder)

```python
# Pass example (useful during development)
for i in range(5):
    if i == 2:
        pass  # TODO: Add logic later
    else:
        print(i)
```

#### 4. else with Loops

Python allows an `else` clause with loops. It executes when the loop completes normally (not via break).

```python
# else with for loop
for i in range(5):
    print(i)
else:
    print("Loop completed successfully")

# else doesn't execute with break
for i in range(5):
    if i == 3:
        break
    print(i)
else:
    print("This won't print")
```

### Do-While Loop Simulation

Python doesn't have a built-in do-while loop, but we can simulate it:

```python
# Simulating do-while (executes at least once)
while True:
    number = int(input("Enter a positive number: "))
    if number > 0:
        print("Thank you!")
        break
    print("Please enter a positive number")
```

### Practice Exercises

**Exercise 36:** Print all numbers from 1 to 100.
```python
# Solution:
for i in range(1, 101):
    print(i)
```

**Exercise 37:** Calculate the factorial of a number using a for loop.
```python
# Solution:
num = int(input("Enter a number: "))
factorial = 1

for i in range(1, num + 1):
    factorial *= i

print(f"Factorial of {num} is {factorial}")
```

**Exercise 38:** Print the Fibonacci sequence up to n terms using a while loop.
```python
# Solution:
n = int(input("How many terms? "))
a, b = 0, 1
count = 0

while count < n:
    print(a, end=" ")
    a, b = b, a + b
    count += 1
print()
```

**Exercise 39:** Find the sum of all even numbers between 1 and 100.
```python
# Solution:
total = 0
for i in range(2, 101, 2):
    total += i
print("Sum of even numbers:", total)  # Output: 2550
```

**Exercise 40:** Create a number guessing game. Generate a random number and let the user guess until they get it right.
```python
# Solution:
import random

secret_number = random.randint(1, 100)
attempts = 0

while True:
    guess = int(input("Guess the number (1-100): "))
    attempts += 1
    
    if guess < secret_number:
        print("Too low! Try again.")
    elif guess > secret_number:
        print("Too high! Try again.")
    else:
        print(f"Congratulations! You got it in {attempts} attempts!")
        break
```

**Exercise 41:** Print a pyramid pattern using nested loops.
```python
# Solution:
rows = 5
for i in range(1, rows + 1):
    # Print spaces
    for j in range(rows - i):
        print(" ", end="")
    # Print stars
    for k in range(2 * i - 1):
        print("*", end="")
    print()
# Output:
#     *
#    ***
#   *****
#  *******
# *********
```

**Exercise 42:** Create a program that prints all prime numbers between 1 and 50.
```python
# Solution:
print("Prime numbers between 1 and 50:")
for num in range(2, 51):
    is_prime = True
    for i in range(2, int(num ** 0.5) + 1):
        if num % i == 0:
            is_prime = False
            break
    if is_prime:
        print(num, end=" ")
print()
```

**Exercise 43:** Reverse a number using a while loop.
```python
# Solution:
num = int(input("Enter a number: "))
reversed_num = 0

while num > 0:
    digit = num % 10
    reversed_num = reversed_num * 10 + digit
    num = num // 10

print("Reversed number:", reversed_num)
```

**Exercise 44:** Print the multiplication table for numbers 1 to 10.
```python
# Solution:
for i in range(1, 11):
    print(f"\nMultiplication table for {i}:")
    for j in range(1, 11):
        print(f"{i} x {j} = {i * j}")
```

**Exercise 45:** Count the number of digits in a number.
```python
# Solution:
num = int(input("Enter a number: "))
count = 0
temp = num

while temp > 0:
    temp = temp // 10
    count += 1

print(f"Number of digits in {num}: {count}")
```

---
