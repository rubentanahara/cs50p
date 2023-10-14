# CS50 - Introduction to programming with Python

- In the terminal, you can excute `nv hello.py` to start coding.
- Type `print("Hello, world")`
- To run your program, run the following command in the terminal `python hello.py` and press enter.

Recall, computers really only understand zeros and ones. Therefore, when you run `python hello.py`, python will interpret the text that you created in `hello.py` and translate it to zeros and ones that the computer can understand.

## Functions

- Functions are verbs or actions that the computer will already know to perform
- In your `hello.py` program, the `print`function knows how to print to the terminal.
- The `print` functions takes arguments. In this case, `"Hello, world"` are the arguments that the `print` function takes.

## Bugs

- Bugs are a natural part of coding. These are mistakes, problems for you to solve. Is part of the process.
- Often, theerror messages will inform you of your mistake and provide you clues on how to fix them. However, there will be many times that the compiler is no this kind.

## Improve your code

- We can add another function called `input`. is a function that takes a prompt as an argument. The new code:

```python
input("Whats your name?")
print("Hello, world")
```

This program doesn't allow to output what your user inputs. For that we need to introuuce you to variables

## Variables

- A variable is just a container fora value within you own program.

```python linenos
name = input("What's your name?")
```

`=` (**assing value to a variable**)

```python linenos
name = input("What's your name?")
print("Hello,")
print(name)
```

## Comments

- Comments are a way for programmers to track what they are doing in ther programs and even inform others about their intentions for a block of code. Basically, they are notes for yourself and others.
- To add comments we use `#`

```python
# Ask the user for their name
name = input("What's your name?")
print("Hello,")
print(name)
```

Also can serve as to-do list for you! 🙌.

## Pseudocode

Is a important type of of comment that becomes a special type of to - do list, especially when you don't understand how to accomplish a coding task.

```python
# Ask the user for their name
name = input("What's your name? ")

# Print hello
print("hello,")

# Print the name inputted
print(name)

"""
this a multine line
comment
"""
```

## Improve your code

Edit your code as follow:

```python
# Ask the user for their name
name = input("What's your name? ")

# Print hello and the inputted name
print("hello, " + name)
```

- it turns out that some functions take many arguments
- We can use a comma `,` to pass in multiple args by editing our code

```python
# Ask the user for their name
name = input("What's your name? ")

# Print hello and the inputted name
print("hello,", name)
```

Both make the same output. Success! ✅

## Strings and Paremeters

- A string, know as a `str` in Python, is a sequence of text.
- Reading the docs of `print` you will notice we cn learn al ot about the arguments that the functions takes.
- Looking at this documentation, you’ll learn that the print function automatically include a piece of code `end='\n'. This \n indicates that the print function will automatically create a line break when run. The print function takes an argument called end` and the default is to create a new line.

```python
# Ask the user for their name
name = input("What's your name? ")
print("hello,", end="")
print(name)
```

Parameter, therefore, are arguments that can be taken by a function.A small problem with quotation marks
Notice how adding quotation marks as part of your string is challenging.
`print("hello,"friend"")` will not work and the compiler will throw an error.

Generally, there are two approaches to fixing this. First, you could simply change the quotes to single quote marks.
Another, more commonly used approach would be code as `print("hello, \"friend\"").` The backslashes tell the compiler that the following character should be considered a quotation mark in the string and avoid a compiler error.

## Formatting Strings

```python
# Ask the user for their name
name = input("What's your name? ")
print(f"hello, {name}")
```

**This f is a special indicator to Python to treat this string a special way, different than previous approaches we have illustrated in this lecture.**

## More on Strings

- To remove whitespaces from a string, we use `strip`.

```python
# Ask the user for their name
name = input("What's your name? ")

# Remove whitespace from the str
name = name.strip()

# Print the output
print(f"hello, {name}")
```

- Using `title` method, it would title case the user's name:

```python
# Ask the user for their name
name = input("What's your name? ")

# Remove whitespace from the str
name = name.strip()

# Capitalize the first letter of each word
name = name.title()

# Print the output
print(f"hello, {name}")
```

- **Let's go further! 🚀**.

```python
name = input("What's your name? ").strip().title()

# Print the output
print(f"hello, {name}")
```

or

```python
name = input("What's your name? ").strip().title()

first, last = name.split(" ")

# Print the output
print(f"hello, {first} {last}")

```

## Integers or int

- An integer is reffered to as an `int`.
- Operators: `+, -, *, /, %`

```python
x = 1
y = 2

z = x + y

print(z)
```

Naturally, when we run python `calculator.py` we get the result in the terminal window of 3. We can make this more interactive using the input function.

```python
x = input("What's x? ")
y = input("What's y? ")

z = x + y

print(z)

```

The output is incorrect as `12`

Prior, we have seen how the + sign concatenates two strings. Because your input from your keyboard on your computer comes into the compiler as text, it is treated a string. We, therefore, need to convert this input from a string to an integer. We can do so as follows:

```python
x = input("What's x? ")
y = input("What's y? ")

z = int(x) + int(y)

print(z)

```

further:

```python
x = int(input("What's x? "))
y = int(input("What's y? "))

print(x + y)

```

## Readability wins 🏆

_Regardless of what approach you take to a programming task, remember that your code must be readable. You should use comments to give yourself and others clues about what your code is doing. Further, you should create code in a way that is readable._

## Float Basics

- A floating point value is a real number that has point in it, such as `0.52`.

```python
x = float(input("What's x? "))
y = float(input("What's y? "))

print(x + y)

```

- Let’s imagine, however, that you want to round the total to the nearest integer. Looking at the Python documentation for round you’ll see that the available arguments are `round(number[n, ndigits])`. Those square brackets indicate that something optional can be specified by the programmer. Therefore, you could do round(n) to round a digit to its nearest integer. Alternatively, you could code as follows:

```python
# Get the user's input
x = float(input("What's x? "))
y = float(input("What's y? "))

# Create a rounded result
z = round(x + y)

# Print the result
print(z)
```

- Formatting output, instead of seeing `1000` convert to `1,000`:

```python
# Get the user's input
x = float(input("What's x? "))
y = float(input("What's y? "))

# Create a rounded result
z = round(x + y)

# Print the formatted result
print(f"{z:,}")
```

Though quite cryptic, that print(f"{z:,}") creates a scenario where the outputted z will include commas where the result could look like 1,000 or 2,500.

## More on Floats

- Round floating point values:

```python
# Get the user's input
x = float(input("What's x? "))
y = float(input("What's y? "))

# Calculate the result
z = x / y

# Print the result
print(z)
```

```python
# Get the user's input
x = float(input("What's x? "))
y = float(input("What's y? "))

# Calculate the result and round
z = round(x / y, 2)

# Print the result
print(z)
```

- We could also use fstring to format the output as follows:

```python
# Get the user's input
x = float(input("What's x? "))
y = float(input("What's y? "))

# Calculate the result
z = x / y

# Print the result
print(f"{z:.2f}")
```

## Functions -> Def

```python
def hello():
    print("hello")


name = input("What's your name? ")
hello()
print(name)
```

going further:

```python
# Create our own function
def hello(to):
    print("hello,", to)


# Output using our own function
name = input("What's your name? ")
hello(name)
```

- We can change our code to add a default value to hello:

```python
# Create our own function
def hello(to="world"):
    print("hello,", to)


# Output using our own function
name = input("What's your name? ")
hello(name)

# Output without passing the expected arguments
hello()
```

- We don’t have to have our function at the start of our program. We can move it down, but we need to tell the compiler that we have a main function and we have a separate hello function.

```python
def main():

    # Output using our own function
    name = input("What's your name? ")
    hello(name)

    # Output without passing the expected arguments
    hello()


# Create our own function
def hello(to="world"):
    print("hello,", to)

```

But there is a problem ❌

This alone, however, will create an error of sorts. If we run python hello.py nothing happens! The reason for this is that nothing in this code is actually calling the main function and bringing our program to life.

```python
def main():

    # Output using our own function
    name = input("What's your name? ")
    hello(name)

    # Output without passing the expected arguments
    hello()


# Create our own function
def hello(to="world"):
    print("hello,", to)


main()
```

## Returning Values

To retrieve values from a functions we use `return` keyboard

```python
def main():
    x = int(input("What's x? "))
    print("x squared is", square(x))


def square(n):
    return n * n


main()
```

## Summing Up

Through the work of this single lecture, you have learned abilities that you will use countless times in your own programs. You have learned about…

- Creating your first programs in Python
- Functions
- Bugs
- Variables
- Comments
- Pseudocode
- Strings
- Parameters
- Formatted Strings
- Integers
- Principles of readability
- Floats
- Creating your own functions and
- Return values.
