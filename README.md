# Python Basics

## Table of Contents

* [The `print()` Function](#the-print-function)
* [Comments in Python](#comments-in-python)
* [Variables](#variables)
* [Data Types](#data-types)
	* [Strings](#strings)
	* [Numeric Types](#numeric-types)
	* [Sequence Types](#sequence-types)
	* [Mapping Types](#mapping-types)
	* [Booleans](#booleans)
	* [Dataframes](#dataframes)
* [Comparison and Logic Operators](#comparison-and-logic-operators)
* [Loops](#loops)
	* [For-Loops](#for-loops)
	* [While-Loops](#while-loops)
* [Conditionals](#conditionals)


## The `print()` Function

As you begin learning to code in Python, you'll want to check that your code is behaving as expected. One of the ways to do so is to print, well, basically everything. The `print()` function is one of the most widely used functions. Functions are a more complicated aspect of Python, so for now, you just need to know that a function looks something like this: `function()`, where the function name is outside of the parentheses, and the parentheses are there to take arguments. An argument is something you give a function as an input. In this case, our function is `print`, and our argument (input) is "Hello, World!". 

```
print("Hello, World!")
```

Now, try printing your name! In my case, it would look like this:

```
print("Viki")
```

Note that `print(Viki)` does not work, as the absence of quotation marks interprets "Viki" as a variable (we will learn more about variables shortly). Try a few more commands on your own and see what you can do! Note that you can also use single quotations to print as long as the quotations marks flanking the statement are the same style (single vs. double).

## Comments in Python

While this isn't strictly specific to Python, comments are useful for a number of reasons, but primarily because (1) it helps someone else read and understand what your code is doing and (2) it helps the future *you* understand the code you wrote. Organization is key when coding, so comments are a really easy way to facilitate this.

### Inline Comments

One type of comment you can write is an inline comment. This is a comment that occurs in the same line as code that is being run. To add a comment, we use the `#` symbol. Everything after the `#` is interpreted as a comment in Python, so it does not get read or executed. 

```
print("Here is an example of an inline comment") # Inline comment
```

Notice that the output is:

```
Here is an example of an inline comment
```

Here, we see that our comment does not get printed.

### Single Line Comments

While inline comments are helpful, I personally have a preference for single line comments. This acts almost like a header, saying something like:

```
# Print my name
print("Hello, World!")
```

The output should now also print out your name. The reason I prefer single line comments is because it seems more organized. It keeps a nice separation between commentary and functional code, so you don't get overwhelmed looking at your code.

## Variables

When coding, you will likely generate and store lots of information. In order to store the information, we can assign it to a variable. There are a few things we need to know about variables in Python:

* Python does not have a command for declaring a variable. The variable is created the moment you first assign a value to it using the assignment operator: `=`
* You can assign any data type to a variable (we will talk more about data types later)
* Variable names should not contain any spaces (spaces are usually replaced with underscores, which is the case with the variable: pet_names)
* Variable names must begin with a letter or the underscore character (a variable name cannot star with a number)
* Variable names can only contain alpha-numeric characters and underscores (A-z, 0-9, and _)
* Variables are case-sensitive (a and A are different variables)

Here, we will demonstrate some examples of legal and illegal variable names.

```
# Illegal variable names
1animal = "Snake"
an-animal = "Dog"
an animal = "Cat"

# Legal variable names
ananimal = "Budgie"
an_animal = "Iguana"
_an_animal = "Gecko"
anAnimal = "Owl"
AnAnimal = "Fish"
ANANIMAL = "Bunny"
an_animal_1 = "Guinea Pig"
```

Notice how we are using comments to tell ourselves more information about the code. Now, try running this code. You should get an invalid syntax error. Why? Because our variables are illegal! We cannot use that syntax for our variable names. Now, comment out the entire "illegal variables" section and try rerunning your code.

```
'''
# Illegal variable names
1animal = "Snake"
an-animal = "Dog"
an animal = "Cat"
'''

# Legal variable names
ananimal = "Budgie"
an_animal = "Iguana"
_an_animal = "Gecko"
anAnimal = "Owl"
AnAnimal = "Fish"
ANANIMAL = "Bunny"
an_animal_1 = "Guinea Pig"
```

When you rerun the code, you should not get an error. You might also be a little shocked to see that you also have no outputs. This is because we did not put anything in our code that gives us an output. Let's try calling and printing on of our variables:

```
# Legal variable names
ananimal = "Budgie"
an_animal = "Iguana"
_an_animal = "Gecko"
anAnimal = "Owl"
AnAnimal = "Fish"
ANANIMAL = "Bunny"
an_animal_1 = "Guinea Pig"

print(an_animal_1)
```

Rerun your code. You should see the output "Guinea Pig." One thing that's great about variables is that they can be changed! Let's say you've decided you don't like "Guinea Pigs" as part of your list. Change it to another animal:

```
an_animal_1 = "Bear"

print(an_animal_1)
```

Rerun your code. Now your output should be "Bear." 

## Data Types

Each data type has various strengths, associated functions for manipulation, and purposes in code. Since this is supposed to be a short introduction, I just want to provide you with the right names for different data types and how they're presented so you can dive further on your own. 

### Strings

A string is a data type that is a sequence of characters. Even though it can contain numbers, the way a string is formatted tells Python to interpret those characters as characters rather than numbers.

```
# Examples of strings
str1 = "Hello world"
str2 = "Spring is coming!"
str3 = "My dog ate 3 slices of my pizza"
str4 = "I can't believe my dog did that"
```

Notice that we have an apostrophe, a number, and even an exclamation mark in the above statements. Because we follow string formatting (flanking the outside of our string with single or double quotes), Python knows that we are inputting characters inside and that it should interpret it as such. 

Note that there is a `str()` function. We do not want to say anything like `str = x`, as this will override the `str()` function and give errors. For this reason, I add numbers or prefixes to my variables. I used numbers in the above example. If I only have one variable, I would do something like `my_str` instead. This helps prevent overriding functions while also still having informative variable names.

### Numeric Types

Numeric types are data types containing numbers (including whole numbers, decimals, fractions, and complex numbers).

#### Integers

Just like we learn in math class, an integer is any whole number. We cannot have a decimal at all for Python integers, as even something like `1.0` is interpreted as a different data type. Let's take a look at some examples of integers:

```
# Integers
int1 = 1
int2 = 9
int3 = 42
int4 = 558
int5 = 21543215
```

Python language is very delicate. This is incredibly helpful in most cases, but it also means that you have strict guidelines to adhere to. For example, `21543215` and `21,543,215` are different data types. At the end of your "Integers" section, add the following:

```
not_int = 21,543,215

print(int5, type(int5))
print(not_int, type(not_int))
```

Notice that when we add commas, it is now considered a tupple, which is a sequence and not a numeric type anymore. Therefore, if you want to use an integer or set a variable to some integer value, use ONLY numeric characters (0-9).

#### Floats

Similar to an integer, a float is a numeric type. However, floats differ in that they allow us to use decimals and fractions, so we are not limited to using whole numbers when using floats.

```
# Floats
float1 = 1.0
float2 = 3.4
float3 = 74.3
float4 = 9.99999999999
float5 = 1844384.85262
float6 = 3/4
float7 = 9/16
```

### Sequence Types

### Mapping Types

### Booleans

### Dataframes

## Comparison and Logic Operators

## Loops

### For-Loops

### While-Loops

## Conditionals