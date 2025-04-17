## **Introduction to Python**
Python is a high-level, interpreted programming language known for its readability and simplicity.<br>
Versatile and widely used in various domains both in backend and frontend.<br>
Interpreted language that executes line by line.<br>
Has rich library support that is open-source and free.<br>
Platform-independent where the script can run on any operating system.<br>
Dynamically typed where data types of variables do not have to be declared when creating as it infers the type, which makes the code more flexible and easy to work with.

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
Variables are used to store and manipulate data.<br>
They are symbolic names pointing to objects or values in memory.<br>
Defined by assigning them a value using the assignment operator.<br>
Case-sensitive and dynamically typed, allowing type changes through reassignment.<br>
Exist in different scopes (global, local, non-local, or built-in), which affects accessibility.<br>
Can have an unlimited number of variables, limited only by computer memory.<br>

```python
# assigning variables 
name = "Lewis Hamilton "
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
`input()` function takes in user input from the console and always returns a string.<br>
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
Process of converting data of one type to another.<br>

### Implicit Type Casting
Python automatically converts one data type to another when data type is not defined. <br>
Always converts smaller data types to larger data types to avoid the loss of data.

```python
state = 'Delhi'
pin = 1130
value = state + pin

# display new value and resulting data type
print("Value:",value)
print("Data Type:",type(value))
```
### Explicit Type Casting
Users convert the data type of an object to required data type.<br>
Loss of data may occur as user enforce the object to a specific data type.

```python
pincode = 110030
pin_code = str(pincode)

# display resulting data type
print("pincode datatype:",type(pincode))
print("pin_code datatype:",type(pin_code))
```

## **Copying**
Using the `=` operator does not create a new object.<br>
It simply creates a new variable name that references the same object in memory.<br>
Changes made using one variable will affect the other.<br>
Both variables point to the same memory address.<br>

```python
list1 = [1, 2, 3]
list2 = list1  # reference

list2[0] = 99

print("list1:", list1)  # [99, 2, 3]
print("list2:", list2)  # [99, 2, 3]
```

### Shallow Copy
Creates a new outer object, but nested objects are not copied.<br>
Instead, the nested objects are still referenced from the original.<br>
Changes to nested elements will affect both the copy and the original.<br>
Uses the `copy.copy()` function.<br>
Outer object is a new instance while inner objects are still shared.

```python
import copy

list1 = [[1, 2], [3, 4]]
shallow_copy = copy.copy(list1)

shallow_copy[0][0] = 99

print("Original List:", list1)       # [[99, 2], [3, 4]]
print("Shallow Copy:", shallow_copy) # [[99, 2], [3, 4]]
```

### Deep Copy
Creates a completely independent copy, including all nested objects.<br>
Changes made to the deep copy do not affect the original object.<br>
Uses the `copy.deepcopy()` function.<br>
Both outer and inner objects are completely separate.<br>
Safe to modify one without affecting the other

```python
import copy

list1 = [[1, 2], [3, 4]]
deep_copy = copy.deepcopy(list1)

deep_copy[0][0] = 99

print("Original List:", list1)   # [[1, 2], [3, 4]]
print("Deep Copy:", deep_copy)   # [[99, 2], [3, 4]]
```

## **Operators**
Special symbols that perform operations on variables and its values. <br>

Arithmetic : Perform mathematical operations like addition, subtraction, multiplication, etc.
```python
x = 10
y = 5

print(x + y)  # addition
print(x - y)  # subtraction
print(x * y)  # multiplication
print(x / y)  # division
print(x % y)  # modulus
print(x ** y) # exponentiation
print(x // y) # floor division
```

Comparison : Compare two values and return a boolean (`True` or `False`).
```python
x = 10
y = 5

print(x == y)  # equal to
print(x != y)  # not equal to
print(x > y)   # greater than
print(x < y)   # less than
print(x >= y)  # greater than or equal to
print(x <= y)  # less than or equal to
```

Logical : Used to combine conditional statements.
```python
x = True
y = False

print(x and y)  # AND
print(x or y)   # OR
print(not x)    # NOT
```

Bitwise : Perform operations at the bit level.
```python
a = 5  # 0101 in binary
b = 3  # 0011 in binary

print(a & b)  # AND
print(a | b)  # OR
print(a ^ b)  # XOR
print(~a)     # NOT
print(a << 1) # left shift
print(a >> 1) # right shift
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

print(a is b)   # true because 'b' refers to 'a'
print(a is c)   # false because 'c' is a different object
print(a is not c) # true because 'c' is not the same object as 'a'
```

Membership : Check if a value is present in a sequence.
```python
fruits = ["apple", "banana", "cherry"]

print("apple" in fruits)   # true 
print("mango" not in fruits) # true
```

## **Conditional Statements**
Conditional statements allow your code to make decisions based on conditions.<br>
Perform different computations and actions depending on whether the condition is True or False.<br>
Common conditional statements include `if`, `elif` (else if), `else`, and `match case`.

### **if statement**
```python
a = 150

if a > 100 and a < 200:
    print("True") # prints statement
else:
    print("False") # skip
```

### **elif statement**
```python
a = 150

if a < 100:
    print("Less than 100") # skip
elif a > 100 and a < 200: 
    print("More than 100 but less than 200") # prints statement
else:
    print("More than 200") # skip
```

### **match case statement**
Similar to switch statements in other programming languages.<br>
Matches a value against multiple case patterns.

```python
def check_day(day):
    match day:
        case "Monday":
            print("Start of the week!") # skip
        case "Friday":
            print("Weekend is near!") # prints statement
        case "Sunday":
            print("Relax, it's Sunday!") # skip
        case _:
            print("It's a regular day.") # skip

check_day("Friday")
```

## **Loops**
Loops are executed for repetitive tasks with conditions.<br>

### **for loop**
Used to iterate over a sequence (e.g., a list, dictionary, or string).

```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print("I love " + fruit)
```

### **while loop**
Continues executing as long as a specified condition is True.

```python
count = 0
while count < 5:
    print("Count: " + str(count))
    count += 1
```

### **do while loop**
Python does not have a built-in `do while` loop, but it can be implemented using `while`.<br>
The loop runs at least once before checking the condition.

```python
i = 1
while True:
    print("Iteration:", i)
    i += 1
    if i > 5:
        break
```

## **Loop Control Statements**
Loop control statements modify the normal sequence of execution in loops.<br>

`break` : Terminates the loop completely when encountered.
```python
for i in range(10):
    if i == 5:
        break  # loop terminates when i is 5
    print(i)
```

`continue` : Skips the rest of the code inside the loop for the current iteration and moves to the next iteration.
```python
for i in range(10):
    if i == 5:
        continue  # skips the iteration when i is 5
    print(i)
```

`pass` : Used as a placeholder for future code, so the loop doesn’t produce an error when no code is written.
```python
for i in range(10):
    if i == 5:
        pass  # placeholder for future implementation
    print(i)
```

## **Errors and Exceptions**
Exceptions are events that occur during the execution of a program and disrupt the normal flow of instructions.<br> 
When an error occurs an exception object is raised.<br>
Exception objects can be handled using exception-handling mechanisms.<br>
Python has several built-in exceptions that indicate different error conditions.

### **Common Exceptions**
`SyntaxError` : Occurs when there is a syntax mistake in the Python code.
```python
print('Hello'  # missing closing parenthesis
```
`TypeError`: Occurs when an operation is performed on an inappropriate data type.
```python
x = 5 + 'Hello'  # adding integer and string
```

`ValueError` : Occurs whn a function receives an arguent of the right type but with an inappropriate value.
```python
num = int('Hello')  # cannot convert string to integer
```
`KeyError` : Occurs when a dictionary key is not found.
```python
d = {'name': 'Alice'}
print(d['age'])  # 'age' key does not exist
```
`IndexError` : Occurs when trying to access an index that is out of range.
```python
list = [1, 2, 3]
print(list[5])  # index out of range
```

`AttributeError` : Occurs when an invalid attribute is accessed on an object.
```python
x = 10
x.append(5)  # integers do not have 'append' method
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
    # some unknown operation that may raise an exception
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
