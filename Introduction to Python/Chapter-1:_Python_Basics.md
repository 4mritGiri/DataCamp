---
Title_Meta: Chapter 1
Course___Title: Python Basics
Course____Description: >-
  An introduction to the basic concepts of Python. Learn how to use Python
  interactively and by using a script. Create your first variables and acquaint
  yourself with Python's basic data types.
Attachments:
  slides_link: 'https://projector-video-pdf-converter.datacamp.com/735/chapter1.pdf'
free_preview: true
lessons:
  - nb_of_exercises: 5
    title: Hello Python!
  - nb_of_exercises: 8
    title: Variables and Types
---

## Hello Python!

---

## The Python Interface

```yaml
type: NormalExercise
key: bdc52f0e19
lang: python
xp: 100
skills:
  - 2
```

In the Python script on the right, you can type Python code to solve the exercises. If you hit _Run Code_ or _Submit Answer_, your python script (`script.py`) is executed and the output is shown in the IPython Shell. _Submit Answer_ checks whether your submission is correct and gives you feedback.

You can hit _Run Code_ and _Submit Answer_ as often as you want. If you're stuck, you can click _Get Hint_, and ultimately _Get Solution_.

You can also use the IPython Shell interactively by simply typing commands and hitting Enter. When you work in the shell directly, your code will not be checked for correctness so it is a great way to experiment.

### `@instructions`
- Experiment in the IPython Shell; type `5 / 8`, for example.
- Add another line of code to the Python script on the top-right (not in the Shell): `print(7 + 10)`.
- Hit _Submit Answer_ to execute the Python script and receive feedback.

### `@hint`
Simply add `print(7 + 10)` in the script on the top-right (not in the Shell) and hit 'Submit Answer'.

### `@pre_exercise_code`
```{python}

```

### `@sample_code`
```{python}
# Example, do not modify!
print(5 / 8)

# Print the sum of 7 and 10

```

### `@solution`
```{python}
# Example, do not modify!
print(5 / 8)

# Put code below here
print(7 + 10)
```

### `@sct`
```{python}
Ex().has_printout(1, not_printed_msg = "__JINJA__:Have you used `{{sol_call}}` to print out the sum of 7 and 10?")
success_msg("Great! On to the next one!")
```

---

## When to use Python?

```yaml
type: MultipleChoiceExercise
key: 9703b117fb
lang: python
xp: 50
skills:
  - 2
```

Python is a pretty versatile language. For which applications can you use Python?

### `@possible_answers`
- You want to do some quick calculations.
- For your new business, you want to develop a database-driven website.
- Your boss asks you to clean and analyze the results of the latest satisfaction survey.
- All of the above.

### `@hint`
Hugo mentioned in the video that Python can be used to build practically any piece of software.

`@pre_exercise_code`
```{python}

```

`@sct`
```{python}
msg1 = "Incorrect. Python can do simple and quick calculations, but it is much more than that!"
msg2 = "Incorrect. There is a very popular framework to build database-driven websites (Django), but Python can do much more."
msg3 = "Incorrect. Python is a powerful tool to do data analysis, but you can also use it for other ends."
msg4 = "Correct! Python is an extremely versatile language."
Ex().has_chosen(4, [msg1, msg2, msg3, msg4])
```

---

## Any comments?

```yaml
type: NormalExercise
key: 7c4a738a13
lang: python
xp: 100
skills:
  - 2
```

Something that Hugo didn't mention in his videos is that you can add **comments** to your Python scripts. Comments are important to make sure that you and others can understand what your code is about.

To add comments to your Python script, you can use the `#` tag. These comments are not run as Python code, so they will not influence your result. As an example, take the comment in the editor, `# Division`; it is completely ignored during execution.

### `@instructions`
Above the `print(7 + 10)`, add the comment 
```
# Addition
```

`@hint`
For this exercise you only have to add one line of comments. It won't run as Python code. Add `# Addition` right above `print(7 + 10)`.

`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}
# Division
print(5 / 8)


print(7 + 10)
```

### `@solution`
```{python}
# Division
print(5 / 8)

# Addition
print(7 + 10)
```

`@sct`
```{python}
Ex().has_code("#\s*(\w+)[\s.!?]*print\s*\(\s*7", not_typed_msg = "Make sure to add the comment right before `print(7 + 10)`.")
success_msg("Great!")
```

---

## Python as a calculator

```yaml
type: NormalExercise
key: 0f7c039428
lang: python
xp: 100
skills:
  - 2
```

Python is perfectly suited to do basic calculations. Apart from addition, subtraction, multiplication and division, there is also support for more advanced operations such as:

- Exponentiation: `**`. This operator raises the number to its left to the power of the number to its right. For example `4**2` will give `16`.
- Modulo: `%`. This operator returns the remainder of the division of the number to the left by the number on its right. For example `18 % 7` equals `4`.

The code in the script gives some examples.

`@instructions`
Suppose you have $100, which you can invest with a 10% return each year. After one year, it's $100 \times 1.1 = 110$ dollars, and after two years it's $100 \times 1.1 \times 1.1 = 121$. Add code to calculate how much money you end up with after 7 years, and print the result.

`@hint`
After two years you have $100 \times 1.1 \times 1.1 = 100 \times 1.1^2$. How much do you have after 7 years than? Use `*` and `**`.

### `@pre_exercise_code`
```{python}
 
```

### `@sample_code`
```{python}
# Addition, subtraction
print(5 + 5)
print(5 - 5)

# Multiplication, division, modulo, and exponentiation
print(3 * 5)
print(10 / 2)
print(18 % 7)
print(4 ** 2)

# How much is your $100 worth after 7 years?

```

### `@solution`
```{python}
# Addition, subtraction
print(5 + 5)
print(5 - 5)

# Multiplication, division, modulo, and exponentiation
print(3 * 5)
print(10 / 2)
print(18 % 7)
print(4 ** 2)

# How much is your $100 worth after 7 years?
print(100 * 1.1 ** 7)
```

`@sct`
```{python}
Ex().has_printout(6, not_printed_msg = "Have you used `print(100 * 1.1 ** 7)` to print out the result of your calculations?")
success_msg("Time for another video!")
```

---

## Variables and Types

```yaml
type: VideoExercise
key: c2e396792e
xp: 50
```

`@projector_key`
433dcfcfedaee070cbf440491c402e3b

---

## Variable Assignment

```yaml
type: NormalExercise
key: 4bf65ad83e
lang: python
xp: 100
skills:
  - 2
```

In Python, a variable allows you to refer to a value with a name. To create a variable use `=`, like this example:

```
x = 5
```

You can now use the name of this variable, `x`, instead of the actual value, `5`.

Remember, `=` in Python means _assignment_, it doesn't test equality!

`@instructions`
- Create a variable `savings` with the value 100.
- Check out this variable by typing `print(savings)` in the script.

`@hint`
- Type `savings = 100` to create the variable `savings`.
- After creating the variable `savings`, you can type `print(savings)`.

`@pre_exercise_code`
```{python}
 
```

`@sample_code`
```{python}
# Create a variable savings


# Print out savings

```

`@solution`
```{python}
# Create a variable savings
savings = 100

# Print out savings
print(savings)
```

`@sct`
```{python}
Ex().check_object("savings").has_equal_value(incorrect_msg="Assign `100` to the variable `savings`.")
Ex().has_printout(0, not_printed_msg = "Print out `savings`, the variable you created, with `print(savings)`.")
success_msg("Great! Let's try to do some calculations with this variable now!")
```

---

## Calculations with variables

```yaml
type: NormalExercise
key: ff06cedeb4
lang: python
xp: 100
skills:
  - 2
```

Remember how you calculated the money you ended up with after 7 years of investing $100? You did something like this:

```
100 * 1.1 ** 7
```

Instead of calculating with the actual values, you can use variables instead. The `savings` variable you've created in the previous exercise represents the $100 you started with. It's up to you to create a new variable to represent `1.1` and then redo the calculations!

`@instructions`
- Create a variable `growth_multiplier`, equal to `1.1`.
- Create a variable, `result`, equal to the amount of money you saved after `7` years. 
- Print out the value of `result`.

`@hint`
- To create the variable `growth_multiplier`, use `growth_multiplier = 1.1`.
- In the example code block of the assignment, replace `100` with `savings` and `1.1` with `growth_multiplier`: `savings * growth_multiplier ** 7`.
- Use the [`print()`](https://docs.python.org/3/library/functions.html#print) function to print the value of a variable.

`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}
# Create a variable savings
savings = 100

# Create a variable growth_multiplier


# Calculate result


# Print out result

```

`@solution`
```{python}
# Create a variable savings
savings = 100

# Create a variable growth_multiplier
growth_multiplier = 1.1

# Calculate result
result = savings * growth_multiplier ** 7

# Print out result
print(result)
```

`@sct`
```{python}
Ex().check_object("savings", missing_msg="The variable `savings` was defined for you, don't remove it!").has_equal_value(incorrect_msg="The variable `savings` should be `100`, like it was defined for you."),
Ex().check_object("growth_multiplier").has_equal_value(incorrect_msg="Did you assign the correct value to `growth_multiplier`?")
Ex().check_correct(
  check_object("result").has_equal_value(incorrect_msg="Have you used `*` and `**` to calculate `result`?"),
  multi(
    has_code("savings\s*\*\s*\(*\s*growth_multiplier", not_typed_msg = "Did you multiply `savings` by `growth_multiplier ** 7`?"),      
    has_code("growth_multiplier\s*\*\*\s*7", not_typed_msg = "Did you raise `growth_multiplier` to the power of `7` using `**`?")   
  )
)

Ex().has_printout(0, not_printed_msg="Remember to print out `result` at the end of your script.")
success_msg("Great!")
```

---

## Other variable types

```yaml
type: NormalExercise
key: 006b48561f
lang: python
xp: 100
skills:
  - 2
```

In the previous exercise, you worked with two Python data types:

- `int`, or integer: a number without a fractional part. `savings`, with the value `100`, is an example of an integer.
- `float`, or floating point: a number that has both an integer and fractional part, separated by a point. `growth_multiplier`, with the value `1.1`, is an example of a float.

Next to numerical data types, there are two other very common data types:

- `str`, or string: a type to represent text. You can use single or double quotes to build a string.
- `bool`, or boolean: a type to represent logical values. Can only be `True` or `False` (the capitalization is important!).

`@instructions`
- Create a new string, `desc`, with the value `"compound interest"`.
- Create a new boolean, `profitable`, with the value `True`.

`@hint`
- To create a variable in Python, use `=`. Make sure to wrap your string in single or double quotes.
- Only two boolean values exist in Python: `True` and `False`. `TRUE`, `true`, `FALSE`, `false` and other versions will not be accepted.

`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}
# Create a variable desc


# Create a variable profitable

```

`@solution`
```{python}
# Create a variable desc
desc = "compound interest"

# Create a variable profitable
profitable = True
```

`@sct`
```{python}
Ex().check_object("desc").has_equal_value()
Ex().check_object("profitable").has_equal_value()
success_msg("Nice!")
```

---

## Guess the type

```yaml
type: MultipleChoiceExercise
key: b35f67514c
lang: python
xp: 50
skills:
  - 2
```

To find out the type of a value or a variable that refers to that value, you can use the [`type()`](https://docs.python.org/3/library/functions.html#type) function. Suppose you've defined a variable `a`, but you forgot the type of this variable. To determine the type of `a`, simply execute:

```
type(a)
```

We already went ahead and created three variables: `a`, `b` and `c`. You can use the IPython shell to discover their type. Which of the following options is correct?

`@possible_answers`
- `a` is of type `int`, `b` is of type `str`, `c` is of type `bool`
- `a` is of type `float`, `b` is of type `bool`, `c` is of type `str`
- `a` is of type `float`, `b` is of type `str`, `c` is of type `bool`
- `a` is of type `int`, `b` is of type `bool`, `c` is of type `str`

`@hint`
Use `type(a)`, `type(b)` and `type(c)` inside the IPython Shell to find out about the variables' types.

`@pre_exercise_code`
```{python}
a = 100*1.1**7
b = "True"
c = False
```

`@sct`
```{python}
msg1 = "The type of `a` is not `int`. Try out `type(a)` and see for yourself."
msg2 = "`b` is not a `bool`, it's a `str`! The fact that `True` is wrapped in double quotes makes it a string."
msg3 = "Correcto perfecto!"
msg4 = "None of the variable's types is correct here. Try `type(a)` and see what type this variable is."
Ex().has_chosen(3,[msg1, msg2, msg3, msg4])
```

---

## Operations with other types

```yaml
type: NormalExercise
key: 4d0d83cc02
lang: python
xp: 100
skills:
  - 2
```

Hugo mentioned that different types behave differently in Python.

When you sum two strings, for example, you'll get different behavior than when you sum two integers or two booleans.

In the script some variables with different types have already been created. It's up to you to use them.

`@instructions`
- Calculate the product of `savings` and `growth_multiplier`. Store the result in `year1`.
- What do you think the resulting type will be? Find out by printing out the type of `year1`.
- Calculate the sum of `desc` and `desc` and store the result in a new variable `doubledesc`.
- Print out `doubledesc`. Did you expect this?

`@hint`
- Assign `growth_multiplier * savings` to a new variable, `year1`.
- To print the type of a variable `x`, use `print(type(x))`.
- Assign `desc + desc` to a new variable, `doubledesc`.
- To print a variable `x`, write `print(x)` in the script.

`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}
savings = 100
growth_multiplier = 1.1
desc = "compound interest"

# Assign product of savings and growth_multiplier to year1


# Print the type of year1


# Assign sum of desc and desc to doubledesc


# Print out doubledesc

```

`@solution`
```{python}
savings = 100
growth_multiplier = 1.1
desc = "compound interest"

# Assign product of savings and growth_multiplier to year1
year1 = savings * growth_multiplier

# Print the type of year1
print(type(year1))

# Assign sum of desc and desc to doubledesc
doubledesc = desc + desc

# Print out doubledesc
print(doubledesc)
```

`@sct`
```{python}
# predefined
msg = "You don't have to change or remove the predefined variables."

Ex().multi(
    check_object('savings', missing_msg=msg).has_equal_value(incorrect_msg=msg),
    check_object('growth_multiplier', missing_msg=msg).has_equal_value(incorrect_msg=msg),
    check_object('desc', missing_msg=msg).has_equal_value(incorrect_msg=msg)
)

# check year1 and printout
Ex().multi(
    check_object("year1").has_equal_value(incorrect_msg="Multiply `savings` and `growth_multiplier` to create the `year1` variable."),
    has_printout(0, not_printed_msg = "__JINJA__:Use `{{sol_call}}` to print out the type of `year1`.")
)

# check doubledesc and printout
Ex().multi(
    check_object("doubledesc").has_equal_value(incorrect_msg  = "Have you stored the result of `desc + desc` in `doubledesc`?"),
    has_printout(1, not_printed_msg = "Don't forget to print out `doubledesc`.")
)

success_msg("Nice. Notice how `desc + desc` causes `\"compound interest\"` and `\"compound interest\"` to be pasted together.")
```

---

## Type conversion

```yaml
type: NormalExercise
key: 085bb602b9
lang: python
xp: 100
skills:
  - 2
```

Using the `+` operator to paste together two strings can be very useful in building custom messages.

Suppose, for example, that you've calculated the return of your investment and want to summarize the results in a string. Assuming the integer `savings` and float `result` are defined, you can try something like this:

```
print("I started with $" + savings + " and now have $" + result + ". Awesome!")
```

This will not work, though, as you cannot simply sum strings and integers/floats.

To fix the error, you'll need to explicitly convert the types of your variables. More specifically, you'll need [`str()`](https://docs.python.org/3/library/functions.html#func-str), to convert a value into a string. `str(savings)`, for example, will convert the integer `savings` to a string.

Similar functions such as [`int()`](https://docs.python.org/3/library/functions.html#int), [`float()`](https://docs.python.org/3/library/functions.html#float) and [`bool()`](https://docs.python.org/3/library/functions.html#bool) will help you convert Python values into any type.

`@instructions`
- Hit _Run Code_ to run the code. Try to understand the error message.
- Fix the code such that the printout runs without errors; use the function [`str()`](https://docs.python.org/3/library/functions.html#func-str) to convert the variables to strings.
- Convert the variable `pi_string` to a float and store this float as a new variable, `pi_float`.

`@hint`
- You should use [`str()`](https://docs.python.org/3/library/functions.html#func-str) twice!
- Use [`float()`](https://docs.python.org/3/library/functions.html#float) on `pi_string` and store the result in `pi_float`.

`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}
# Definition of savings and result
savings = 100
result = 100 * 1.10 ** 7

# Fix the printout
print("I started with $" + savings + " and now have $" + result + ". Awesome!")

# Definition of pi_string
pi_string = "3.1415926"

# Convert pi_string into float: pi_float

```

`@solution`
```{python}
# Definition of savings and result
savings = 100
result = 100 * 1.10 ** 7

# Fix the printout
print("I started with $" + str(savings) + " and now have $" + str(result) + ". Awesome!")

# Definition of pi_string
pi_string = "3.1415926"

# Convert pi_string into float: pi_float
pi_float = float(pi_string)
```

`@sct`
```{python}

# ensure predefined values are unmodified
msg = "You don't have to change or remove the predefined variables."
Ex().multi(
    check_object("savings", missing_msg=msg).has_equal_value(incorrect_msg=msg),
    check_object("result", missing_msg=msg).has_equal_value(incorrect_msg=msg)
)

Ex().check_correct(
    has_printout(0),
    multi(
        check_function("str", 0).check_args(0).has_equal_value(incorrect_msg="Inside the `print()` command, make sure to convert `savings` into a string with `str(savings)`."),
        check_function("str", 1).check_args(0).has_equal_value(incorrect_msg="Inside the `print()` command, make sure to convert `result` into a string `str(result)`.")
    )
)

# check pi_float
Ex().check_correct(
    check_object("pi_float").has_equal_value(),
    multi(
        check_object("pi_string").has_equal_value(),
        check_function("float", missing_msg = "In order to convert `pi_string` to a float, be sure to use the `float()` function.").has_equal_value(incorrect_msg="Use `float(pi_string) to create the variable `pi_float`.")
    )
)

success_msg("Great! You have a profit of around $95; that's pretty awesome indeed!")
```

---

## Can Python handle everything?

```yaml
type: MultipleChoiceExercise
key: 3e5f0bdf3a
lang: python
xp: 50
skills:
  - 2
```

Now that you know something more about combining different sources of information, have a look at the four Python expressions below.
Which one of these will throw an error? You can always copy and paste this code in the IPython Shell to find out!

`@possible_answers`
- `"I can add integers, like "  + str(5) + " to strings."`
- `"I said " + ("Hey " * 2) + "Hey!"`
- `"The correct answer to this multiple choice exercise is answer number " + 2`
- `True + False`

`@hint`
Copy and paste the different expressions into the IPython Shell and try to figure out which one throws an error.

`@pre_exercise_code`
```{python}

```

`@sct`
```{python}
msg1 = "Incorrect, this command runs perfectly fine."
msg2 = "It's perfectly possible to 'multiply strings' in Python..."
msg3 = "Correct! Because you're not converting `2` to a string with [str()](https://docs.python.org/3/library/functions.html#func-str), this will give an error."
msg4 = "`True + False` doesn't error out. Feel free to try it in the console to confirm!"
Ex().has_chosen(3, [msg1, msg2, msg3, msg4])
```
