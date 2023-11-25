Programming Language Project
================

This is an assignment for my programming languages class. My goal is to
make an accessibly-written tutorial for people who are new to
programming. I’m very new to github and R, so please be patient as we
learn together.

Thank you!

## PLP 1 - Getting Started

### A Brief History

R is a programming language and coding environment designed for
statistical computation. It is also a foundation that centers itself
around the goal of public good by providing access to free, open-source
statistical coding software. It was developed in the mid-nineties and
version 1.0 was officially released in 2000. It sits at number 18 on the
TIOBE index (at the time of writing) and is one of the most utilized
languages (if not THE most) in the field of data analytics. Its name is
a reference to its predecessor, S, and doubles as a reference to its
founders, Robert Gentleman and Ross Ihaka, whose names share the letter
as their first initials.

### Usages of R

R is open-source and free on principle, making it a very accessible and
popular tool in statistical education and data analytics. Perhaps its
most popular and powerful trait is its community-driven nature; its
utility is constantly expanded by user-created “packages” that are easy
to install and use for an extremely adaptable experience. That’s not to
say that it only finds usage in independent academics and researchers
though – R is reported to be used for the collection and processing of
user data for giants like Amazon, Meta, and Google. It’s also used by
the FDA and National Weather Service to create models and visualize data
for the public.

### R Resources (R-esources?)

[The R Foundation](https://www.r-project.org/foundation/), [RStudio
(Currently being renovated)](https://www.rstudio.com), and [Book
Recommendations By RStudio](https://www.rstudio.com/resources/books/)

### Downloading and Using R

R can be downloaded from
[r-project.org](https://cran.r-project.org/mirrors.html), and its
signature desktop IDE (Integrated Development Environment – essentially,
the place where you write and run code), RStudio, can be downloaded from
[rstudio.com](https://posit.co/download/rstudio-desktop/), or used as an
online application called [RStudio Cloud](https://posit.cloud/plans). It
is also supported by VSCode (tutorial by VSCode
[here](https://code.visualstudio.com/docs/languages/r)). **All of this
software is available for free!**

### Hello, World!

Time for the time-honored programming tradition of the “Hello, World!”
code! Lucky for us, this one’s simple. With your IDE of choice, use a
print statement:

``` r
print("Hello World!")
--- [1] "Hello World!"
```

### Comments in R

To include human-friendly text within code to clarify things for
non-computer audiences, you can “comment” your code. This text is
ignored by the computer when your program is run.

Unfortunately, R does not currently support multi-line commenting, but
single-line commenting is allowed and a keyboard command makes
commenting out larger sections easy. Use `#` to comment out a single
line like so:

``` r
#Anything I write here is for humans to read
print("This is a sample line of code") #And over here
--- [1] "This is a sample line of code"

# And all these lines
# are "commented out"
# as well
```

For multi-line comments (for example, a block of code you want to
temporarily remove from your program), highlight the section and use the
command `ctrl` + `shift` + `c`

## PLP 2 - Data Types and Naming Conventions

### Naming conventions

In R, “snake_case,” “camelCase,” and “dot.case” are all valid naming
conventions. Typically, snake case and camel case are preferred to avoid
confusion with object-oriented programming languages. Additionally, when
naming functions, the first letter is capitalized to distinguish them
from variables.

Variables should not start with an underscore, a dot, or a number.

Reserve words in R include TRUE, FALSE, NULL, NA, NaN, Inf, if, else,
repeat, while, for, in, function, next, break, NA_character\_,
NA_integer\_, NA_real\_, NA_complex\_, and ellipses (…).

### Variable typing

R is an implicitly typed language, meaning that a variable’s type does
not have to be immediately declared. It is dynamically typed, meaning
that the program only “knows” the variable type once the program is run.
And given its nature as a statistics-based language, it is weakly typed,
meaning that it will generally accommodate the programmer’s wishes when
asked to execute operations between data types (ie. a float and an
integer).

### Types of variables

- Strings: Essentially, text variables. Written in quotes.
- Numerics: Variables that are numbers, including integers (which are
  exclusively whole numbers, written with a capital L immediately
  following the value) and floats (variables that are numbers that
  either have decimal points or may have them later, no special notation
  needed)
- Lists: A list of variables (of any type) that are stored together.
  Written in parentheses and separated by commas
- Boolean values: Variables used for logical operations: TRUE and FALSE
- Hashes: Similar to a list, but each item has a corresponding item
  attached to it. This data type is often called a “dictionary” in other
  languages due to its “key/definition” structure. This requires the
  “hash” package, which means you need to run the command
  `library(hash)` before creating a hash.

Examples:

``` r
## Strings

string <- "string"
print(string)
--- [1] "string"
```

``` r
## Numerics (Integer)

numericint <- 5L
print(numericint)
--- [1] 5
```

``` r
## Numerics (Float)

numericfloat <- 5.5
print(numericfloat)
--- [1] 5.5
```

``` r
## Interactions between types of numerics

print(numericint + numericfloat)
--- [1] 10.5
print(numericint * numericfloat)
--- [1] 27.5
print(numericint / numericfloat)
--- [1] 0.9090909
```

``` r
## Lists

list <- list(2, 4, 6, 8)
print(list)
--- [[1]]
--- [1] 2
--- 
--- [[2]]
--- [1] 4
--- 
--- [[3]]
--- [1] 6
--- 
--- [[4]]
--- [1] 8
```

``` r
## Booleans

booleant <- TRUE
print(booleant)
--- [1] TRUE

booleanf <- FALSE
print(booleanf)
--- [1] FALSE
```

``` r
## Hashes

library(hash)

hashexample <- hash()
hashexample[["key1"]] <- "val1"
hashexample[["key2"]] <- "val2"
hashexample[["key3"]] <- "val3"
print(hashexample)
--- <hash> containing 3 key-value pair(s).
---   key1 : val1
---   key2 : val2
---   key3 : val3
```

### Variable interactions

Since R is a weakly typed language, it does offer more possibilities for
interactions between variables than other languages. For example,
integers and floats can interact without being converted. You can also
combine variable types in a single list.

``` r
snlist1 <- list("1", 2, 3)
snlist2 <- list(1, 2.5, 3)

print(snlist1)
--- [[1]]
--- [1] "1"
--- 
--- [[2]]
--- [1] 2
--- 
--- [[3]]
--- [1] 3
print(snlist2)
--- [[1]]
--- [1] 1
--- 
--- [[2]]
--- [1] 2.5
--- 
--- [[3]]
--- [1] 3
```

However, R will not allow operations between numbers in string format
(for example: “1” as opposed to 1 or 1L)

``` r
x = "1" + 2
--- Error in "1" + 2: non-numeric argument to binary operator
print(2)
--- [1] 2

# Will throw error: "non-numeric argument to binary operator"
```

### Operations

As a math-based language, it’s important to know the arithmetic
operators in R:

- Addition: `+`
- Subtraction: `-`
- Multiplication: `*`
- Division: `/`
- Exponents: `^`
- Division (returns the remainder): `%%`
- Integer division: `%/%`

Notably, assignment operations in R are typically written as
`variable <- value` or `value -> variable` rather than a single equal
sign.

There are also logical operators and comparisons: - Equal-to: `==` -
Not-equal-to: `!=` - Less-than: `<` - Greater-than: `>` - Less-than or
equal-to: `<=` - Greater-than or equal-to: `>=` - AND (both are TRUE):
`&` - OR (at least one is TRUE): `|`

(P.S.: R has secret extra symbols for AND and OR – see the README
section “Short circuiting” for more info)

``` r
## Arithmetic operations

1+2     # Addition
--- [1] 3
1-2     # Subtraction
--- [1] -1
1*2     # Multiplication
--- [1] 2
1/2     # Division
--- [1] 0.5
1^2     # Exponents
--- [1] 1
1%%2    # Division remainder
--- [1] 1
1L%/%2L # Integer division
--- [1] 0
```

``` r
## Logical operations & comparisons

1+2 == 3  # Equal to
--- [1] TRUE
1+2 != 3  # Not equal to
--- [1] FALSE

1<2 # Less than
--- [1] TRUE
1>2 # Greater than
--- [1] FALSE

1<=2  # Less than or equal to
--- [1] TRUE
1>=2  # Greater than or equal to
--- [1] FALSE
```

``` r
1 == 1 & 2 == 2   # 1 is equal to 1 AND 2 is equal to 2
--- [1] TRUE
1 != 1 & 2 == 2   # 1 is not equal to 1 AND 2 is equal to 2
--- [1] FALSE

1 == 1 | 2 == 2   # 1 is equal to 1 OR 2 is equal to 2 (TRUE, TRUE)
--- [1] TRUE
1 != 1 | 2 == 2   # 1 is not equal to 1 OR 2 is equal to 2 (FALSE, TRUE)
--- [1] TRUE
1 != 1 | 2 != 2   # 1 is not equal to 1 OR 2 is not equal to 2 (FALSE, FALSE)
--- [1] FALSE
```

## PLP 3 - Functions

### Declaring a function in R

The syntax to declare a function is
`yourFunctionName <- function(parameters) {definition}`. Functions must
be declared before (above) they are called in the code. R does not allow
functions to return more than one value, but it does support the ability
to pass multiple parameters of different types into a function. It also
allows recursive (self-calling) functions.

``` r
multitype <- function(a, b)
{
  return(paste(a, b))
}

multitype("a", 3)
--- [1] "a 3"
```

``` r
factfunct <- function(val)
{
  if(val < 1)
  {
    return(1)
  }
  else
  {
    return(val * factfunct(val-1))
  }
}

factfunct(4)
--- [1] 24
```

``` r
factof5 <- factfunct(5)
print(factof5)
--- [1] 120
```

### Pass-by-reference or pass-by-value?

Whether a language is “pass-by-reference” or “pass-by-value” determines
what happens when you assign a variable to another variable. Depending
on the language’s design, it may copy the value of the old variable into
the new one (pass-by-value) or it may create the new variable as an
alias of the old variable that will reflect any changes that occur to it
(pass-by-reference). We can tell which protocol a language uses by
assigning an old variable to a new variable, changing the value of the
old variable, and then checking the value of the new variable. If the
new value changed with the old variable, the language is
pass-by-reference. If the new variable holds the value that the old
variable initially started with, it is pass-by-value. As you can see in
this example, R is a pass-by-value language.

``` r
old <- 3

new <- old

old = 4

print(new)
--- [1] 3
```

### Scope

R is a statically scoped language, meaning that when it encounters
“free,” unassigned variables, it searches within the smallest possible
environment first and then expands its search outward. For example, if
the variable <x> is called in function `function1`, which resides in the
function `main`, R would first search for `x` in `function1`, then
`main`, then through the “search” list. This list always begins with the
global environment (the space outside all of your functions), is
followed by any packages that you’ve loaded into your program, and ends
with the “base” R code. This order can be modified and may be relevant
if there are objects with the same name in different packages.

## PLP 4 - Selection, Loops, and Conditionals

### Boolean values & condition statements

R’s boolean values are `TRUE` and `FALSE`. Its conditional statements
are `if`, `else if`, and `else`, which are written as follows:

    # Not actual R code!

    if(condition 1){
      action 1
    } else if(condition 2) {
      action 2
    } else {
      action 3
    }

The braces and `else if` option help to prevent the “dangling else”
ambiguity, in which consecutive “if” statements are followed by an
“else” and the program must decide which “if” statement it belongs to.

``` r
trueval <- TRUE
falseval <- FALSE

if(trueval == TRUE){
  print("trueval is true")
} else {
  print("trueval is false")
}
--- [1] "trueval is true"

if(falseval == TRUE){
  print("falseval is true")
} else {
  print("falseval is false")
}
--- [1] "falseval is false"
```

``` r
if(trueval == TRUE & falseval == FALSE){
  print("trueval is true and falseval is false")
} else if(falseval == TRUE){
  print("both values are true")
} else if(trueval == FALSE){
  print("both values are false")
} else {
  print("trueval is false and falseval is true")
}
--- [1] "trueval is true and falseval is false"
```

### Short circuiting

Short circuiting allows a program to take “shortcuts” in certain cases
of logical condition statements. For example, given that `T` is TRUE and
`F` is FALSE:

In the case of `if(T OR F)`: a program only needs one of the two
statements to be TRUE in order to proceed. Since the first item is TRUE,
it doesn’t matter what the second item is; the condition for the OR
statement has been met. If a language uses short circuit logic, the
program would skip over the second item and go straight to the
designated code block. **This statement short circuits.**

In the case of `if(F OR T)`: the program needs to see that the second
item is TRUE in order for the condition to be met. **This statement does
not short circuit.**

In the case of `if(F AND T)`: the program needs both items to be TRUE in
order to proceed. Since it can tell from the first item that this cannot
be the case, it will skip over the second item and not execute the
designated code block. **This statement short circuits.**

In the case of `if(T AND F)`: the program needs to see that the second
item is FALSE before it can know that the condition is not met. **This
statement does not short circuit.**

In R, we get extra versions of the logical operators that indicate AND
and OR – whereas `&` and `|` do NOT allow short circuiting, the logical
operators `&&` and `||` do! You can see the difference (and the
potential consequences) of using one set or the other in the stopIt
example in the following examples.

``` r
stopIt <- function(){
  stop("NOT short circuited!")
}
  
if(1 == 1 || stopIt()){
  print("short circuited!")
}
--- [1] "short circuited!"

if(1 == 1 | stopIt()){
  print("short circuited!")
}
--- Error in stopIt(): NOT short circuited!
```

### Switch

The “switch” function in R allows you to evaluate an expression against
any number of “cases” and choose the appropriate path. It takes in an
expression, cases, and sometimes an optional default case.

The first type of switch statement has a string as its expression. Its
syntax is as follows:

    # Not actual R code!

    expression <- "string2"

    switch(expression,
          "string1" = "case1",
          "string2" = "case2,
          "string3" = "case3,
          "default case") # The default case is optional. If not specified, an unmatched expression will return NULL

    # The program will proceed with action2. If the expression was, for example, "string4", or "stringABC", it would proceed with "default case".

Interactive example:

``` r
switchboard <- function(route){
  switch(direction,
         "northwest" = "take track 1",
         "north" = "take track 2",
         "northeast" = "take track 3",
         "this direction is not available")
}

direction <- "north"
print(switchboard(direction))
--- [1] "take track 2"
```

``` r
direction <- "northeast"
print(switchboard(direction))
--- [1] "take track 3"
```

``` r
direction <- "east"
print(switchboard(direction))
--- [1] "this direction is not available"
```

The second type has an integer as its expression. It does not allow for
the option of a default case. It will proceed with the case that has the
index of the expression integer. Syntax:

    # Not actual R code!

    expression <- 1

    switch(expression,
          "case1",
          "case2",
          "case3",
          "case4")

    # The program will proceed with "case1" -- remember, R starts counting at 1!

Interactive example:

``` r
switchnum <- function(expression)
  switch(expression,
         "option a",
         "option b",
         "option c",
         "option d")

exp <- 1

print(switchnum(exp))
--- [1] "option a"
```

``` r
exp <- 5

print(switchnum(exp))
--- NULL
```

## PLP 5 - Classes and Inheritance

If you’re coming to R from python, you might be curious about the
potential for object-oriented programming in R. It’s possible!

“Objects” are like variables that can hold multiple attributes, for
example, a “student” object that holds a first name string, last name
string, and a student ID number. Objects belong to “classes” that
contain “methods,” which are functions that can be used on its objects.
If you’re new to this, I recommend trying out the examples before trying
to understand it perfectly. It makes more sense once you get started!
The “reference class” example is most similar to what you might see in
other languages, so don’t be afraid to start there, especially if you’ve
got python or java experience.

### Classes in R

Leave it to R, the program with five different assignment operators, to
have three types of classes. These types are S3, S4, and reference
classes.

#### S3

S3 is the simplest, least strict, and most commonly used type of class
in R. Its objects hold their attributes in specially-structured lists.

Syntax:

    # Not actual R code!

    objectName = list(attribute1=value1, attribute2=value2, attributeN=valueN)

    class(objectName) <- "ClassName"

Example:

``` r
cat1 = list(name="Claire", age=7, type="domestic shorthair")
cat2 = list(name="Francis", age=7, type="silly little guy")

class(cat1) <- "Cats"
class(cat2) <- "Cats"
```

As an example of S3 methods, lets write a function that prints a “Cats”
object nicely. Right now, printing a “Cats” object would return this:

``` r
print(cat1)
--- $name
--- [1] "Claire"
--- 
--- $age
--- [1] 7
--- 
--- $type
--- [1] "domestic shorthair"
--- 
--- attr(,"class")
--- [1] "Cats"
```

We can give R a “Cats” class-specific version of the generic print
function that returns its attributes in a more readable format like so:

``` r
# To access an S3 object's attributes, use objectName$attribute

print.Cats <- function(objcat) {
  cat(objcat$name, "\n")
  cat(objcat$age, "year-old", objcat$type, "\n")
}

print(cat1)
--- Claire 
--- 7 year-old domestic shorthair
print(cat2)
--- Francis 
--- 7 year-old silly little guy
```

This print function will only affect objects in the class “Cats”.

#### S4

An S4 class also stores its objects’ attributes in lists, but it has a
formalized structure for creating classes and objects.

Syntax:

    # Not actual R code!

    setClass("ClassName", slots=list(attribute1=valueType, attribute2=valueType, attributeN=valueType))

    objectName = new("ClassName", attribute1=value1, attribute2=value2, attributeN=valueN)

Example:

``` r
setClass("Dogs", slots=list(name="character", age="numeric", type="character"))

dog1 = new("Dogs", name="Louie", age=13, type="good boy")
dog2 = new("Dogs", name="Goose", age=11, type="silly goose")
```

#### Reference Classes

This is the system that will be most familiar to object-oriented
programmers. Its methods belong to the class itself rather than generic
functions.

Syntax:

    # Not actual R code!

    setRefClass("ClassName", fields=list(attribute1=valueType, attribute2=valueType, attributeN=valueType), methods=list(definitions))

    objectName <- ClassName(attribute1=value1, attribute2=value2, attributeN=valueN)

Example:

``` r
Chickens <- setRefClass("Chickens", 
                        fields=list(name="character", age="numeric", type="character"),
                        methods=list(
                          birthday = function(){
                            age <<- (age + 1)
                            cat("happy birthday!", name, "is now", age, "\n")
                          }
                        ))

chicken1 <- Chickens(name="Gwen", age=5, type="porcelain duccles")
chicken2 <- Chickens(name="Inari", age=3, type="easter egger")
chicken3 <- Chickens(name="Paprika", age=3, type="buff brahma bantam")
chicken4 <- Chickens(name="Chichi", age=3, type="easter egger")
```

``` r
print(chicken3$age)
--- [1] 3
chicken3$birthday()
--- happy birthday! Paprika is now 4
print(chicken3$age)
--- [1] 4
```

### Inheritance

Classes can be connected through inheritance, in which a “parent” class
is extended by a “child” class that has all the same attributes and
methods but adds some of its own. Let’s say there’s an airport keeping
track of its employees’ information. All employees have an ID, a first
name, and a last name. Pilots also have a pilot license number. We could
use an “employees” class to store employee IDs and names that is
extended by a “pilots” class to store pilot license numbers.

#### S3

Syntax:

    # Not actual R code!

    class(object) <- c("ChildClassName", "ParentClassName")

Example:

``` r
e1s3 <- list(firstName="Abby", lastName="Andrews", id=1)
e2s3 <- list(firstName="Belinda", lastName="Brooks", id=2)
p1s3 <- list(firstName="Ciara", lastName="Clark", id=3, licenseNum=100)

class(e1s3) <- "EmployeesS3"
class(e2s3) <- "EmployeesS3"
class(p1s3) <- c("EmployeesS3", "PilotsS3")
```

#### S4

Syntax:

    #Not actual R code!

    setClass("ChildClassName",
      slots=list(childClassAttributes)),
      contains="ParentClassName")

Example:

``` r
setClass("EmployeesS4", 
         slots=list(firstName="character", lastName="character", id="numeric"))

setClass("PilotsS4",
         slots=list(licenseNum="numeric"),
         contains="EmployeesS4")

e1s4 <- new("EmployeesS4",
          firstName="Alex", lastName="Adams", id=10)
e2s4 <- new("EmployeesS4",
          firstName="Bailey", lastName="Brown", id=11)
p1s4 <- new("PilotsS4",
          firstName="Cassandra", lastName="Castillo", id=12, licenseNum=101)
```

#### Reference Classes

Syntax:

    ChildClassName <- setRefClass("ChildClassName",
      fields=list(childClassAttributes),
      contains="ParentClassName")

Example:

``` r
EmployeesRC <- setRefClass("EmployeesRC",
                        fields=list(firstName="character", lastName="character", id="numeric"))

PilotsRC <- setRefClass("PilotsRC",
                      fields=list(licenseNum="numeric"),
                      contains="EmployeesRC")

e1RC <- EmployeesRC(firstName="Alessandra", lastName="Alvarez", id=201)
e2RC <- EmployeesRC(firstName="Bernard", lastName="Baker", id=202)
p1RC <- PilotsRC(firstName="Catherine", lastName="Collins", id=203, licenseNum=102)
```
