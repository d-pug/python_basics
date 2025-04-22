# Python Basics

I have primarily adapted the content presented here from a [Python Focus Group](https://github.com/vhaghani26/python_focus_group) I conducted to teach students during grad school. 

## Table of Contents

* [The `print()` Function](#the-print-function)
* [Comments in Python](#comments-in-python)
* [Variables](#variables)
* [Data Types](#data-types)
	* [Strings](#strings)
	* [Numeric Types](#numeric-types)
	* [Sequence Types](#sequence-types)
	* [Mapping Types (Dictionaries)](#mapping-types-dictionaries)
	* [Booleans](#booleans)
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

The `print()` function is essential for troubleshooting, as it allows you to check outputs and variables, data types, and even just allows you to print progress notes during script execution. In my opinion, the troubleshooting aspect is most helpful. As you write your scripts, you want to make sure the inputs and outputs are what you expect at every stage, so you can print them for verification.

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

Variables are fundamental in Python as they store data values that can be referenced and manipulated throughout your code. They enable you to create dynamic programs by allowing you to hold and update information, making your code more flexible and efficient. Whenever possible, assign information/data to a variable, ideally with an informative name, so people can easily read and understand your code. Using variables also allows you to easily reuse and edit code you have already written.

## Data Types

Each data type has various strengths, associated functions for manipulation, and purposes in code. Since this is supposed to be a short introduction, I just want to provide you with the right names for different data types and how they're presented so you can dive further on your own. 

### Strings

A string is a data type that is a sequence of characters. Even though it can contain numbers, the way a string is formatted tells Python to interpret those characters as characters rather than numbers. They enable people to handle inputs, format outputs, and work with textual data in a flexible manner. Often times, when you work with data frames, your data will be stored as a string. You can manipulate your data based on its contents and even manipulate the contents themselves. Strings are also used to represent file names and paths.

```
# Examples of strings
str1 = "Hello world"
str2 = "Spring is coming!"
str3 = "My dog ate 3 slices of my pizza"
str4 = "I can't believe my dog did that"

print(str1)
```

Notice that we have an apostrophe, a number, and even an exclamation mark in the above statements. Because we follow string formatting (flanking the outside of our string with single or double quotes), Python knows that we are inputting characters inside and that it should interpret it as such. 

Note that there is a `str()` function. We do not want to say anything like `str = x`, as this will override the `str()` function and give errors. For this reason, I add numbers or prefixes to my variables. I used numbers in the above example. If I only have one variable, I would do something like `my_str` instead. This helps prevent overriding functions while also still having informative variable names.

### Numeric Types

Numeric types are data types containing numbers (including whole numbers, decimals, fractions, and complex numbers). They provide the foundation for performing mathematical operations, statistical analysis, and data manipulation. Whether working with integers for counting and indexing or using floats for precise calculations and measurements, numeric types allow you to handle a wide range of numerical data effectively. In data frame operations, such as those performed with libraries like Pandas or Polars, numeric types are used for aggregating, filtering, and analyzing datasets.

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
int5 = 21543215
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

# View types
print(float1)
print(type(float1))

# View types
print(float4)
print(type(float4))
```

### Sequence Types

Sequence types represent collections of data where each item is accessible by its index. Sequence types are fundamental for storing and manipulating data presented in a specific order. There are multiple types of sequence types, including tupples, lists, ranges, bytearrays, etc. Here, I will be focusing on lists and ranges because these are more commonly used sequence types.

Sequence types are extremely helpful in Python, as they provide a structured way to store and manipulate collections of data. Lists, for instance, allow for dynamic data management, so you can easily add, remove, or modify elements while maintaining order. This flexibility is essential for tasks like data analysis, where the ability to handle varying data types and structures is necessary. Ranges, on the other hand, facilitate efficient iteration and generation of sequences, making them particularly useful in loops and mathematical computations.

#### Lists

Lists are ordered sequences represented with square brackets. They can contain strings, floats, integers, other lists, and even other data types. You can even make a list of data frames. Let's look at some examples:

```
# Make a list
list1 = ["Viki", "Shawn", "Sophia", "David"]
print(list1)

# Include multiple data types in a list
list2 = ["Lamp", 3, 7.2, True, (1, 2, 3)]
print(list2)
```

As mentioned earlier, the elements in a list use a specific order (index). To access indexed components, you use the number corresponding to the order the data is presented in. It is important to note that Python is 0-based, so to access the first element, we can use the index 0.

```
# Index a list
print(list2[0])
print(list2[0][0])
print(list2[-1])
print(list2[4][1])
```

Lists are dynamic, meaning you can add, remove, or change items if needed:

```
# Appending to a list
my_fav_artists = ["Michael Jackson", "Metallica", "Guns N Roses"]
my_fav_artists.append("Billy Idol")
print(my_fav_artists)

# Delete element
del(my_fav_artists[0])
print(my_fav_artists)

# Change list element
my_fav_artists[0] = "Billy Joel"
print(my_fav_artists)
```

#### Ranges

The `range()` function returns a sequence of numbers.

```
# Turn our range into a list
numbers = list(range(1,6))
print(numbers)
```

Let's take a look at our output more closely. Notice that our list starts with "1" and ends with "5." This is the same behavior we notice with indexing; our last digit has an off-by-one behavior. This means we have to add one to the last digit to get the range we want. For example, if we want the numbers 1-20 in a list, we have to use the following:

```
# Turn our range into a list containing numbers 1-20
range1_20 = list(range(1,21))
print(range1_20)
```

We can also tell Python to skip numbers in a given range. The notation is `(first number in range, last number in range + 1, every Xth value you want)`. Now let's put this in action. Let's try to view all even numbers in the range 1 through 10.

```
# Even numbers from 1-10
even_numbers=list(range(2,11,2))
print(even_numbers)
```

If we look more closely at the information in the range function, we see that we start at 2. Why not 1? This is because adding a value to skip other values accounts for the first value already. This command is basically us saying "Starting at 2 and ending at 11, skip every 2nd number." In this case, beginning our range with 1 means that our second element, 2, would be skipped instead.

### Mapping Types (Dictionaries)

Mapping types are data types used to associate keys and values. Dictionaries are the only built-in mapping type, but others can be found in the `collections` module, such as `deafultdict`, `OrderedDict`, `Counter`, etc.

Dictionaries are a type of collection in Python. It has keys and values, where a key is analogous to the index. To create a dictionary, we use curly brackets: `{}`. The keys have to be immutable and unique (since they act as an index), but the values can be immutable, mutable, and duplicates. Each key and value pair is separated by a comma. One of the strengths of dictionaries is that they are known to be really efficient for data storage and manipulation. If you're working with a lot of data at once and need something to run quickly, a dictionary is a good way to go Let's make a dictionary!

```
# Make our first dictionary
dict1 = {'a':0, 'b':1, 'c':2}
print(dict1)
```

You can use several data types as the values in a dictionary.

```
# Mix data types in a dictionary
dict2 = {"my_string":"Coffee", "my_int": 8, "my_float":9.2, "my_list":[1, 2, 3, 4, 5]}
print(dict2)
```

We can search for values in a dictionary like we would use indexing.

```
# Find values in a dictionary
dict3 = {
  "brand": "Honda",
  "model": "Civic",
  "year": 2020
}
print(dict3["brand"])
```

We can add new entries using the assignment operator `=`.

```
# Add new value dictionary entry
dict3["owner"] = "Sadie"
print(dict3)
```

We can also delete entries.

```
# Delete dictionary entry
del(dict3["owner"])
print(dict3)
```

### Booleans

While Boolean values are usually not directly coded for, they are extremely helpful since any logical operator or statement ends up being a Boolean output. Booleans are most heavily associated with conditionals (i.e. `if` statements). A Boolean value can take two on two values: True or False. 

```
bool1 = type(True)
print(bool1)
```

We can also use numerics to represent a Boolean value, where 1 represents True and 0 represents False:

```
# Demonstrate Boolean as integer
bool2 = int(True)
print(bool2)
bool3 = int(False)
print(bool3)
```

## Comparison and Logic Operators

Comparison and logic operators allow you to evaluate conditions and make decisions based on the results, facilitating control over your script and associated data handling. By allowing for the combination of multiple conditions, these operators allow for the creation of complex and dynamic logical expressions, which is essential when you create a script that can have multiple different types of inputs.

### Comparison Operators

Comparison operators compare some value or operand, then, based on some condition, produce a Boolean.

We can use the equality operator, `==` to determine if values are equal.

```
# Variables
a = 5
b = 10
c = 5

# Determine if values are equal
IsEqual = a == b
print(IsEqual)
```

Let's compare the magnitude of the values.

```
# Check if a value is greater than another
IsGreater = a > b
print(IsGreater)

# Check if a value is less than another
IsLess = a < b
print(IsLess)

# Check if a value is less than or equal to another
IsLessOrEqual = a <= c
print(IsLessOrEqual)

# Check if a value is greater than or equal to another
IsGreaterOrEqual = b >= c
print(IsGreaterOrEqual)
```

Testing for equality is easy, but now how do we test for inequality using operators? In Python, we can use the inequality operator: `!=`.

```
# See if values are not equal
IsNotEqual1 = a != b
print(IsNotEqual1)

IsNotEqual2 = a != c
print(IsNotEqual2)
```

### Logic Operators

Logic operators take Boolean values and produce different Boolean values. The "not," "or," and "and" operator takes in two values to produce a new Boolean value. You can use "if, and" and "if, or" statements. The "and" statement is only True when both conditions are true. The "or" statement is true if one condition is True. The "not" statement outputs the opposite true value. This is essentially what we see in a [truth table](https://docs.oracle.com/html/E79061_01/Content/Reference/Truth_tables.htm). Let's take a look at these.

```
# Basic logic operators
print(not(True))
print(not(False))
```

The following example uses a conditional (if statement), which we will dive into later. I will keep it basic here, but wanted to demonstrate the logic used.

```
# Using logic operators in a basic conditional
album_year = 1983
if album_year > 1979 and album_year < 1990:
	print("This album was made in the 80’s")
```

## Loops

### For-Loops

We can perform an action on every component of various data types (e.g. lists, dictionaries, tuples, sets, strings) using a for-loop function. The concept can be thought of as "for every item, do this action." This is called iteration. It allows you to carry out many actions at once instead of doing it individually for objects, variables, or data. It is one of the most widely and commonly used tools in Python. Regarding syntax, after the initial "for" statement, every indented line following the for/in command is considered inside the loop, and each indented line is executed once for each value in the list. While this may sound a little complicated, it is far easier understood in practice. 


```
# Make a list
magicians = ["alice", "david", "carolina"]

# Printing the list to see the magicians
print(magicians)

# Printing each magician individually
for magician in magicians:
	print(magician)
```

Notice how the outputs are different. This is because the for loop carried out the print function for each element in the list rather than printing the whole list. Let's try another for-loop!

```
# Carry out more complicated actions
for magician in magicians:
	print(magician.title() + ", that was a great trick!")
	print("I can’t wait to see your next trick, " + magician.title() + ".\n")
```

If we want to do something after a for-loop, write the code without an indentation. You can also include a line break if you prefer to keep the code cleaner.

```
# Carry out more complicated actions
for magician in magicians:
	print(magician.title() + ", that was a great trick!")
	print("I can’t wait to see your next trick, " + magician.title() + ".\n")
	
print("Thank you, everyone. That was a great magic show!")
```

Here are some more examples of basic for-loops. Including how you can implement the `range()` function.

```
# More basic for-loops
A = [1, 2, 3, 4, 5]
for value in A:
    print(value)
	
dates = [1982, 1980, 1973]
for date in dates:
    print(date)
	
# A more complicated for-loop where you can access the index and list items
x = len(dates)
for i in range(x):
    print(i, dates[i])  
	
# The range() function
squares = []
for value in range(1,11):
	square = value**2
	squares.append(square)
print(squares)
```

### While-Loops

While-loops are similar to for-loops, but instead of executing a statement a set number of times, a while loop will only run if a condition is met. This is especially helpful if you want to iterate a certain number of times.

```
# Basic while-loop with 10 iterations
i = 0
while i < 10:
	print(i)
	i += 1

# A while-loop with two variables
x = 11
y = 1
while y < x:
	print(y)
	y += 1
```

Be careful with while-loops, however, as it is easy to get stuck in one. Below is an example of a never ending while-loop.

```
# Broken while-loop
i = 0
while i < 10:
	print(i)
```

Here are some examples:

```
# More complicated while-loop
dates = [1982, 1980, 1973, 2000]
i = 0
year = 0
while year != 1973:
    year = dates[i]
    i = i + 1
    print(year)
print("It took ", i ,"repetitions to get out of loop.")

# Another complicated while-loop
PlayListRatings = [10, 9.5, 10, 8, 7.5, 5, 10, 10]
i = 1
Rating = PlayListRatings[0]
while Rating >= 6:
    print(Rating)
    Rating = PlayListRatings[i]
    i += 1

# One last while-loop for reference
squares = ['orange', 'orange', 'purple', 'blue ', 'orange']
new_squares = []
i = 0
while squares[i] == 'orange':
    new_squares.append(squares[i])
    i += 1
print(new_squares)
```

## Conditionals

What exactly is a conditional? Well, a conditional is when you want to carry out a certain set of actions only if something (data in this case) meets a certain condition. For example, if the weather is sunny out, then I will wear shorts. Otherwise, I will wear long pants. 

Now what about data? In many situations, our data is dynamic and we want to carry out different operations given a set of conditions. Additionally, you can define conditions based on nearly all data types. Let's dive in and see what we can do with conditionals!

Imagine you are at a club that requires you to be 18 years old to enter. Let's simulate this scenario in code. Try running the following in your script and let's see the output.

```
age = 19

if age >= 18:
    print("You may enter!")
else:
    print("You are too young to enter.")
```

Upon running it, we see that since the age is 19, we may enter! What if our age is not 19? Let's change the age to 16 and run it again. You should now see a different response. This is the power of the conditional - different code is executed based on what condition gets met.

```
age = 16

if age >= 18:
    print("You may enter!")
else:
    print("You are too young to enter.")
```

Generally speaking, conditionals have the following structure:

```
if {some condition}:
    {code to execute}
else:
    {alternative code to execute if the condition is not met}
```

Aside from simply carrying out code, you can also use the variable in the code:

```
age = 14
print("Dad: Happy birthday! How old are you turning this year?")
print(f"Son: Thank you. I’m turning {age} this year")
if age >= 16:
	print("Dad: Good, now go get a job")
else:
	print(f"Dad: Wow, only {16-age} more years until you can get a job")
```

There may be times when you have more than two possible paths to execute depending on the data. In this case, you can add an `elif` statement. `elif` stands for "else if," essentially meaning "if it doesn't match the first condition, see if it matches this one." It makes more sense in action, so let's take a look. Below, we will check to see the status of `x` in relation to `y`.

```
x = 5
y = 10

if x > y:
    print("x is greater than y")
elif x < y:
    print("x is less than y")
else:
    print("x is equal to y")
```

Change the values of `x` and `y` and see how the outputs change.