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

## Conditionals

- Built within Python are a set of “operators” that can are used to ask mathematical questions.
- > and < symbols are probably quite familiar to you.
- > = denotes “greater than or equal to.”
- <= denotes “less than or equal to.”
- == denotes “equals, though do notice the double equal sign! A single equal sign would assign a value. Double equal signs are used to compare variables.
- != denotes “not equal to.
  Conditional statements compare a left-hand term to a right-hand term.

## If Statement

```python

x = int(input("What's x? "))
y = int(input("What's y? "))

if x < y:
    print("x is less than y")

```

- Then, the `if` statement compares x and y. If the condition of `x < y` is met, the print statement is executed.

- If statements use `bool` or boolean values (true or false) to decide whether or not to execute. If the statement of `x > y` is true, the compiler will register it as true and execute the code.

## Control Flow, elif, and else

```python
x = int(input("What's x? "))
y = int(input("What's y? "))

if x < y:
    print("x is less than y")
if x > y:
    print("x is greater than y")
if x == y:
    print("x is equal to y")

```

We can improve the code:

```python

x = int(input("What's x? "))
y = int(input("What's y? "))

if x < y:
    print("x is less than y")
elif x > y:
    print("x is greater than y")
elif x == y:
    print("x is equal to y")

```

Notice how the use of elif allows the program to make less decisions. First, the if statement is evaluated. If this statement is found to be true, all the elif statements not be run at all. However, if the if statement is evaluated and found to be false, the first elif will be evaluated. If this is true, it will not run the final evaluation.

There is one final improvement we can make to our program. Notice how logically elif x == y is not a necessary evaluation to run. After all, if logically x is not less than y AND x is not greater than y, x MUST equal y. Therefore, we don’t have to run elif x == y. We can create a “catch-all,” default outcome using an else statement. We can revise as follows:

```python
x = int(input("What's x? "))
y = int(input("What's y? "))

if x < y:
    print("x is less than y")
elif x > y:
    print("x is greater than y")
else:
    print("x is equal to y")

```

## or

`or` allows your program to decide between one or more alternatives. For example, we could further edit our program as follows:

```python
x = int(input("What's x? "))
y = int(input("What's y? "))

if x < y or x > y:
    print("x is not equal to y")
else:
    print("x is equal to y")
```

we can make an improvement:

```python
x = int(input("What's x? "))
y = int(input("What's y? "))

if x == y:
    print("x is equal to y")
else:
    print("x is not equal to y")

```

Notice that the == operator evaluates if what is on the left and right are equal to one another. That use of double equal signs is very important. If you use only one equal sign, an error will likely be thrown by the compiler.

## and

Similar to or, and can be used within conditional statements.

```python
score = int(input("Score: "))
if score >= 90 and score <= 100:
    print("Grade: A")
elif score >=80 and score < 90:
    print("Grade: B")
elif score >=70 and score < 80:
    print("Grade: C")
elif score >=60 and score < 70:
    print("Grade: D")
else:
    print("Grade: F")
```

We could improve our code as follows:

```python
  score = int(input("Score: "))

  if 90 <= score <= 100:
      print("Grade: A")
  elif 80 <= score < 90:
      print("Grade: B")
  elif 70 <= score < 80:
      print("Grade: C")
  elif 60 <= score < 70:
      print("Grade: D")
  else:
      print("Grade: F")
```

```python
score = int(input("Score: "))

if score >= 90:
    print("Grade: A")
elif score >= 80:
    print("Grade: B")
elif score >= 70:
    print("Grade: C")
elif score >= 60:
    print("Grade: D")
else:
    print("Grade: F")
```

## Modulo

```python
x = int(input("What's x? "))

if x % 2 == 0:
    print("Even")
else:
    print("Odd")
```

## Creating Our Own Parity Function

We can create our own function to check whether a number is even or odd. Adjust your code as follows:

```
def main():
    x = int(input("What's x? "))
    if is_even(x):
        print("Even")
    else:
        print("Odd")


def is_even(n):
    if n % 2 == 0:
        return True
    else:
        return False


main()
```

## Pythonic

In the programming world, there are types of programming that are called “Pythonic” in nature. That is, there are ways to program that are sometimes only seen in Python programming. Consider the following revision to our progra

```python
def main():
    x = int(input("What's x? "))
    if is_even(x):
        print("Even")
    else:
        print("Odd")


def is_even(n):
    return True if n % 2 == 0 else False


main()
```

We can further revise our code and make it more and more readable:

```python
def main():
    x = int(input("What's x? "))
    if is_even(x):
        print("Even")
    else:
        print("Odd")


def is_even(n):
    return n % 2 == 0


main()
```

## match

Consider the following program:

```python
name = input("What's your name? ")

if name == "Harry":
      print("Gryffindor")
  elif name == "Hermione":
      print("Gryffindor")
  elif name == "Ron":
      print("Gryffindor")
  elif name == "Draco":
      print("Slytherin")
  else:
      print("Who?")
```

Notice the first three conditional statements print the same response.

improvment:

```python
 name = input("What's your name? ")

  if name == "Harry" or name == "Hermione" or name == "Ron":
      print("Gryffindor")
  elif name == "Draco":
      print("Slytherin")
  else:
      print("Who?")
```

Alternatively, we can use match statements to map names to houses. Consider the following code:

```python
 name = input("What's your name? ")

  match name:
      case "Harry":
          print("Gryffindor")
      case "Hermione":
          print("Gryffindor")
      case "Ron":
          print("Gryffindor")
      case "Draco":
          print("Slytherin")
      case _:
          print("Who?")
```

Notice the use of the \_ symbol in the last case. This will match with any input, resulting in similar behavior as an else statement.

A match statement compares the value following the match keyword with each of the values following the case keywords. In the event a match is found, the respective indented code section is executed and the program stops the matching.
We can improve the code:

```python
 name = input("What's your name? ")

  match name:
      case "Harry" | "Hermione" | "Ron":
          print("Gryffindor")
      case "Draco":
          print("Slytherin")
      case _:
          print("Who?")
```

Notice, the use of the single vertical bar |. Much like the or keyword, this allows us to check for multiple values in the same case statement.

You now have the power within Python to use conditional statements to ask questions and have your program take action accordingly. In this lecture, we discussed…

- `Conditionals`
- `if Statements`
- `Control flow, elif, and else`
- `or`
- `and`
- `Modulo`
- `Creating your own function`
- `Pythonic coding`
- `and match`

# Iterations

## Loops

- Essentially, loops are a way to do something over and over again

```python
print("meow")
print("meow")
print("meow")
```

- Loops enable you to create a block of code that executes over and over again.

## While loops

- The while loop is nearly universal throughout all coding languages.
- Such a loop will repeat a block of code over and over again.
- In the text editor window, edit your code as follows:

```python
i = 3
while i != 0:
    print("meow")
```

Notice how even though this code will execute print("meow") multiple times, it will never stop! It will loop forever. while loops work by repeatedly asking if the condition of the loop has been fulfilled. In this case, the compiler is asking “does i not equal zero?” When you get stuck in a loop that executes forever, you can press control-c on your keyboard to break out of the loop.

To fix :

```python
i = 3
while i != 0:
  print("meow")
  i = i - 1
```

to decrease:

```python
 i = 1
  while i <= 3:
      print("meow")
      i = i + 1
```

```python
i = 0
while i < 3:
    print("meow")
    i += 1
```

## For loops

A `for` loop is a different type of loop.

To best understand a for loop, it’s best to begin by talking about a new variable type called a list in Python. As in other areas of our lives, we can have a grocery list, a to-do list, etc.

```python

for i in [0, 1, 2]:
    print("meow")

```

Notice how clean this code is compared to your previous while loop code. In this code, i begins with 0, meows, i is assigned 1, meows, and, finally, i is assigned 2, meows, and then ends.

While this code accomplishes what we want, there are some possibilities for improving our code for extreme cases. At first glance, our code looks great. However, what if you wanted to iterate up to a million? It’s best to create code that can work with such extreme cases. Accordingly, we can improve our code as follows:

```python
for i in range(3):
    print("meow")

```

Notice how range(3) provides back three values (0, 1, and 2) automatically. This code will execute and produce the intended effect, meowing three times.

Our code can be further improved. Notice how we never use i explicitly in our code. That is, while Python needs the i as a place to store the number of the iteration of the loop, we never use it for any other purpose. In Python, if such a variable does not have any other significance in our code, we can simply represent this variable as a single underscore \_. Therefore, you can modify your code as follows:

```python
for _ in range(3):
    print("meow")
```

Notice how changing the i to \_ has zero impact on the functioning of our program.

Our code can be further improved. To stretch your mind to the possibilities within Python, consider the following code:

```python
print("meow" * 3)
```

Notice how it will meow three times, but the program will produce meowmeowmeow as the result. Consider: How could you create a line break at the end of each meow?

Indeed, you can edit your code as follows:

```python
print("meow\n" * 3, end="")
```

Notice how this code produces three meows, each on a separate line. By adding end="" and the \n we tell the compiler to add a line break at the end of each meow.

## Improving with user input

We can use loops as a way of validating the input of the user.

A common paradigm within Python is to use a while loop to validate the input of the user.

```python
while True:
    n = int(input("What's n? "))
    if n < 0:
        continue
    else:
        break
```

Notice that we’ve introduced two new keywords in Python, continue and break. continue explicitly tells Python to go to the next iteration of a loop. break, on the other hand, tells Python to “break out” of a loop early, before it has finished all of its iterations. In this case, we’ll continue to the next iteration of the loop when n is less than 0—ultimately reprompting the user with “What’s n?”. If though, n is greater than or equal to 0, we’ll break out of the loop and allow the rest of our program to run.

# Lists

```python
students = ["Hermione","Harry","Ron"]

print(students[0])
...
...

```

We can use loops to iterates over the list
https://docs.python.org/3/tutorial/datastructures.html#more-on-lists

```python
students = ["Hermione","Harry","Ron"]

for s in students:
    print(s)
```

# Length

We can use `len` as a way of checking the length of the list called students

```python
students = ["Hermoine", "Harry", "Ron"]

for i in range(len(students)):
    print(i + 1, students[i])
```

Notice how executing this code results in not only getting the position of each student plus one using i + 1, but also prints the name of each student. len allow you to dynamically see how long the list of the students is regardless how much it grows.

https://docs.python.org/3/library/functions.html?highlight=len#len

# Dictionaries

- dicts or dictionaries is a data structure that allows you to associate keys with values
- Where a list is a list of multiple values, a dict associates a key with a value.

```python
students = ["Hermoine", "Harry", "Ron", "Draco"]
houses = ["Gryffindor", "Gryffindor", "Griffindor", "Slytherin"]
```

However, this can become quite cumbersome as our lists grow!

```python
students = {
    "Hermoine": "Gryffindor",
    "Harry": "Gryffindor",
    "Ron": "Gryffindor",
    "Draco": "Slytherin",
}
print(students["Hermoine"])
print(students["Harry"])
print(students["Ron"])
print(students["Draco"])
```

Notice how we use {} curly braces to create a dictionary. Where lists use numbers to iterate through the list, dicts allow us to use words.

if you want to print the names of the students :

```python
for student in students:
    print(student)
```

print both key and value

```python
for student in students:
    print(student, students[student])
```

list of dicts

```python
students = [
    {"name": "Hermoine", "house": "Gryffindor", "patronus": "Otter"},
    {"name": "Harry", "house": "Gryffindor", "patronus": "Stag"},
    {"name": "Ron", "house": "Gryffindor", "patronus": "Jack Russell terrier"},
    {"name": "Draco", "house": "Slytherin", "patronus": None},
]

for student in students:
    print(student["name"], student["house"], student["patronus"], sep=", ")
```

Dictionaries docs: https://docs.python.org/3/tutorial/datastructures.html#dictionaries
