## **Introduction to Python**
- Python is a high-level, interpreted programming language known for its readability and simplicity.
- Versatile and widely used in various domains both in backend and frontend.
- Interpreted language that executes line by line.
- Has rich library support that is open-source and free.
- Platform-independent where the script can run on any operating system.
- Dynamically typed where data types of variables do not have to be declared when creating as it infers the type, which makes the code more flexible and easy to work with.

```python
# print a message
print("Hello, World!")
```

## **Comments**

`#` : Use for single comment 

`"""` : Use for multiple line comment
```python
# single line comment

"""
multiple line 
comment
"""
```

## **Variables**
- Variables are used to store and manipulate data.
- They are symbolic names pointing to objects or values in memory.
- Defined by assigning them a value using the assignment operator.
- Case-sensitive and dynamically typed, allowing type changes through reassignment.
- Exist in different scopes (global, local, non-local, or built-in), which affects accessibility.
- Can have an unlimited number of variables, limited only by computer memory.

```python
# assigning variables 
word = "Evangelion"
number = 30
coefficient = 32.09
fruits = ["apple", "watermelon", "mango"]
colours = ("Blue", "Green", "Red")
ordinals = {1: "first", 2: "second", 3: "third"}

# variables can also refer to custom objects like an instance of a class
class CustomClass:
    pass
instance = CustomClass()
```

## **Input and Output**
`input()` function takes in user input from the console and always returns a string.

`print()` function displays the output in the console.

```python
# input function
name = input("Enter your name: ")
age = int(input("Enter your age: "))

# output function
print(f"Hello, {name}!")
print(f"You are {age} yrs old")
```

## **Data Types**

Text Type:	`str`
```python
# string 
name = "John"
alphanumeric = "Code2301AB"
```

Numeric Types:	`int`, `float`, `complex`
```python
# integer
age = 30

# float
height = 6.1

# complex 
complex = 23 + 3j
```

Sequence Types:	`list`, `tuple`, `range`
```python
# list
fruits = ["apple", "watermelon", "grapes"]

# tuple
fruits = ("apple", "watermelon", "grapes")	

# range
numbers = range(5, 15)  
```

Mapping Type:	`dict`
```python
# dictionary
person = {"name": "Alice", "age": 25}
```    

Set Types:	`set`, `frozenset`
```python
# set
colours = {"green", "blue", "red"}	    

#frozenset
colours = frozenset({"green", "blue", "red"})	
```    

Boolean Type:	`bool`
```python
# boolean
a = True
b = False
```    

Binary Types:	`bytes`, `bytearray`, `memoryview`
```python
# bytes
a = b"Greetings"

# bytearray		
a = bytearray(5)

# memoryview		
a = memoryview(bytes(5))		
```    

None Type:	`NoneType`
```python
x = None
```

## **Type Casting**

- Process of converting data of one type to another.
- There are two types of type conversion

### Implicit Type Casting
- Python automatically converts one data type to another when data type is not defined. 
- Always converts smaller data types to larger data types to avoid the loss of data.

```python
state = 'Delhi'
pin = 1130
value = state + pin

# display new value and resulting data type
print("Value:",value)
print("Data Type:",type(value))
```
### Explicit Type Casting
- Users convert the data type of an object to required data type.
- Loss of data may occur as user enforce the object to a specific data type.

```python
pincode = 110030
pin_code = str(pincode)

# display resulting data type
print("pincode datatype:",type(pincode))
print("pin_code datatype:",type(pin_code))
```

## **Operators**
- Special symbols that perform operations on variables and values. 

Arithmetic : Perform mathematical operations like addition, subtraction, multiplication, etc.
```python
x = 10
y = 5

print(x + y)  # Addition
print(x - y)  # Subtraction
print(x * y)  # Multiplication
print(x / y)  # Division
print(x % y)  # Modulus
print(x ** y) # Exponentiation
print(x // y) # Floor division
```

Comparison : Compare two values and return a boolean (`True` or `False`).
```python
x = 10
y = 5

print(x == y)  # Equal to
print(x != y)  # Not equal to
print(x > y)   # Greater than
print(x < y)   # Less than
print(x >= y)  # Greater than or equal to
print(x <= y)  # Less than or equal to
```

Logical : Used to combine conditional statements.
```python
x = True
y = False

print(x and y)  # Logical AND
print(x or y)   # Logical OR
print(not x)    # Logical NOT
```

Bitwise : Perform operations at the bit level.
```python
a = 5  # 0101 in binary
b = 3  # 0011 in binary

print(a & b)  # AND
print(a | b)  # OR
print(a ^ b)  # XOR
print(~a)     # NOT
print(a << 1) # Left Shift
print(a >> 1) # Right Shift
```

Assignment : Used to assign values to variables.
```python
x = 10
x += 5  # x = x + 5
x -= 3  # x = x - 3
x *= 2  # x = x * 2
x /= 4  # x = x / 4
x %= 3  # x = x % 3
x **= 2 # x = x ** 2
x //= 2 # x = x // 2
```

Identity : Used to compare memory locations of objects.
```python
a = [1, 2, 3]
b = a
c = [1, 2, 3]

print(a is b)   # True because 'b' refers to 'a'
print(a is c)   # False because 'c' is a different object
print(a is not c) # True because 'c' is not the same object as 'a'
```

Membership : Check if a value is present in a sequence.
```python
fruits = ["apple", "banana", "cherry"]

print("apple" in fruits)   # True
print("mango" not in fruits) # True
```

## **Conditional Statements**
- Conditional statements allow your code to make decisions based on conditions.
- Perform different computations and actions depending on whether the condition is True or False.
- Common conditional statements include `if`, `elif` (else if), `else`, and `match case`.

### **if statement**
```python
a = 150

if a > 100 and a < 200:
    print("True")
else:
    print("False")
```

### **elif statement**
```python
a = 150

if a < 100:
    print("Less than 100")
elif a > 100 and a < 200:
    print("More than 100 but less than 200")
else:
    print("More than 200")
```

### **match case statement**
- Similar to switch statements in other programming languages.
- Matches a value against multiple case patterns.

```python
def check_day(day):
    match day:
        case "Monday":
            print("Start of the week!")
        case "Friday":
            print("Weekend is near!")
        case "Sunday":
            print("Relax, it's Sunday!")
        case _:
            print("It's a regular day.")

check_day("Friday")
```

## **Loops**
- Loops are executed for repetitive tasks with conditions.
- Common looping methods are `for`, `while`, and `do while`.

### **for loop**
- Used to iterate over a sequence (e.g., a list, dictionary, or string).

```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print("I love " + fruit)
```

### **while loop**
- Continues executing as long as a specified condition is True.

```python
count = 0
while count < 5:
    print("Count: " + str(count))
    count += 1
```

### **do while loop**
- Python does not have a built-in `do while` loop, but it can be implemented using `while`.
- The loop runs at least once before checking the condition.

```python
i = 1
while True:
    print("Iteration:", i)
    i += 1
    if i > 5:
        break
```

## **Loop Control Statements**
- Loop control statements modify the normal sequence of execution in loops.

`break` : Terminates the loop completely when encountered.
```python
for i in range(10):
    if i == 5:
        break  # Loop terminates when i is 5
    print(i)
```

`continue` : Skips the rest of the code inside the loop for the current iteration and moves to the next iteration.
```python
for i in range(10):
    if i == 5:
        continue  # Skips the iteration when i is 5
    print(i)
```

`pass` :Used as a placeholder for future code, so the loop doesn’t produce an error when no code is written.
```python
for i in range(10):
    if i == 5:
        pass  # Placeholder for future implementation
    print(i)
```

## **Errors and Exceptions**
- Exceptions are events that occur during the execution of a program and disrupt the normal flow of instructions. 
- When an error occurs an exception object is raised.
- Exception objects can be handled using exception-handling mechanisms.
- Python has several built-in exceptions that indicate different error conditions.

### **Common Exceptions**
`SyntaxError` : Occurs when there is a syntax mistake in the Python code.
```python
print('Hello'  # Missing closing parenthesis
```
`TypeError`: Occurs when an operation is performed on an inappropriate data type.
```python
x = 5 + 'Hello'  # Adding integer and string
```

`ValueError` : Occurs whn a function receives an arguent of the right type but with an inappropriate value.
```python
num = int('Hello')  # Cannot convert string to integer
```
`KeyError` : Occurs when a dictionary key is not found.
```python
d = {'name': 'Alice'}
print(d['age'])  # 'age' key does not exist
```
`IndexError` : Occurs when trying to access an index that is out of range.
```python
list = [1, 2, 3]
print(list[5])  # Index out of range
```

`AttributeError` : Occurs when an invalid attribute is accessed on an object.
```python
x = 10
x.append(5)  # Integers do not have 'append' method
```

`ImportError / ModuleNotFoundError` : Occurs when an import statement fails.
```python
import nonexistent_module
```

### **Exception Handling using `try-except`**
```python
try:
    print(10 / 0)
except ZeroDivisionError:
    print("Cannot divide by zero!")
```

### **Handling Multiple Exceptions**
```python
try:
    x = int("Hello")
except (ValueError, TypeError) as e:
    print(f"Error occurred: {e}")
```

### **Using `else` and `finally`**
```python
try:
    num = int(input("Enter a number: "))
    result = 10 / num
except ZeroDivisionError as e:
    print(f"Error occurred: {e}")
except ValueError as e:
    print(f"Invalid input. Error: {e}")
else:
    print(f"Result: {result}")
finally:
    print("Execution completed.")
```

### **Identifying Unknown Errors**
If you do not know what exception may occur, you can catch all exceptions using a generic `Exception` block.
```python
try:
    # Some unknown operation that may raise an exception
    x = 10 / 0
except Exception as e:
    print(f"An unexpected error occurred: {e}")
```

### **Raising Exceptions Manually**
```python
x = -5
if x < 0:
    raise ValueError("Negative numbers are not allowed")
```
