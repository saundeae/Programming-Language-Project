# Programming Language Project
Hello, world! This is an assignment for my programming languages class. My goal is to make an accessibly-written tutorial for people who are new to programming. I'm very new to github and R, so please be patient as we learn together.

Thank you!

## PLP I - Getting Started

### A Brief History
R is a programming language and coding environment designed for statistical computation. It is also a foundation that centers itself around the goal of public good by providing access to free, open-source statistical coding software. It was developed in the mid-nineties and version 1.0 was officially released in 2000. It sits at number 18 on the TIOBE index (at the time of writing) and is one of the most utilized languages (if not THE most) in the field of data analytics. Its name is a reference to its predecessor, S, and doubles as a reference to its founders, Robert Gentleman and Ross Ihaka, whose names share the letter as their first initials.

### Usages of R
R is open-source and free on principle, making it a very accessible and popular tool in statistical education and data analytics. Perhaps its most popular and powerful trait is its community-driven nature; its utility is constantly expanded by user-created "packages" that are easy to install and use for an extremely adaptable experience. That's not to say that it only finds usage in independent academics and researchers though -- R is reported to be used for the collection and processing of user data for giants like Amazon, Meta, and Google. It's also used by the FDA and National Weather Service to create models and visualize data for the public.

### R Resources (R-esources?)
[The R Foundation](https://www.r-project.org/foundation/), 
[RStudio (Currently being renovated)](https://www.rstudio.com), and 
[Book Recommendations By RStudio](https://www.rstudio.com/resources/books/)

### Downloading and Using R
R can be downloaded from [r-project.org](https://cran.r-project.org/mirrors.html), and its signature desktop IDE (Integrated Development Environment -- essentially, the place where you write and run code), RStudio, can be downloaded from [rstudio.com](https://posit.co/download/rstudio-desktop/). The IDE is also available as an online application called [RStudio Cloud](https://posit.cloud/plans). For the purposes of this project, I will be using VSCode as my IDE (tutorial by VSCode [here](https://code.visualstudio.com/docs/languages/r)). **All of this software is available for free!**

### Hello, World!
Time for the time-honored programming tradition of the "Hello, World!" code! Lucky for us, this one's simple. With your IDE of choice, use a print statement:

```
print("Hello, World!")
```

### Comments in R
"Commenting" in programming is the act of writing "human-friendly" text within code to clarify things for non-computer audiences. This text is ignored by the computer when your program is run.

Unfortunately, R does not currently support multi-line commenting, but single-line commenting is allowed and a keyboard command makes commenting out larger sections easy. Use "#" to comment out a single line like so:

```
#Anything I write here is for humans to read
print("This is a sample line of code") #And over here
#And over here too

# And all these lines
# are "commented out"
# as well :)
```

For multi-line comments (for example, a block of code you want to temporarily remove from your program), highlight the section and use the command "ctrl + shift + c"

## PLP 2 - Data Types and Naming Conventions

### Naming conventions

In R, "snake_case," "camelCase," and "dot.case" are all valid naming conventions. Typically, snake case and camel case are preferred to avoid confusion with object-oriented programming languages. Additionally, when naming functions, the first letter is capitalized to distinguish them from variables.

Variables should not start with an underscore, a dot, or a number.

Reserve words in R include TRUE, FALSE, NULL, NA, NaN, Inf, if, else, repeat, while, for, in, function, next, break, NA_character_, NA_integer_, NA_real_, NA_complex_, and ellipses (...).

### Variable typing

R is an implicitly typed language, meaning that a variable's type does not have to be immediately declared. It is dynamically typed, meaning that the program only "knows" the variable type once the program is run. And given its nature as a statistics-based language, it is weakly typed, meaning that it will generally accommodate the programmer's wishes when asked to execute operations between data types (ie. a float and an integer).

### Types of variables
- Strings: Essentially, text variables. Written in quotes.
- Numerics: Variables that are numbers, including integers (which are exclusively whole numbers, written with a capital L immediately following the value) and floats (variables that are numbers that either have decimal points or may have them later, no special notation needed)
- Lists: A list of variables (of any type) that are stored together. Written in parentheses and separated by commas
- Boolean values: Variables used for logical operations: TRUE and FALSE
- Hashes: Similar to a list, but each item has a corresponding item attached to it. This data type is often called a "dictionary" in other languages due to its "key/definition" structure.

All types listed here have interactive examples in the Rmd (R Markdown) file called PLP2.Rmd

### Variable interactions

Since R is a weakly typed language, it does offer more possibilities for interactions between variables than other languages. For example, integers and floats can interact without being converted. You can also combine variable types in a single list (Examples of all in PLP2.Rmd)

However, R will not allow operations between numbers in string format (for example: "1" as opposed to 1 or 1L)

### Operations

As a math-based language, it's important to know the artithmetic operators in R:

- Addition: +
- Subtraction: -
- Multiplication: *
- Division: /
- Exponents: ^
- Division (returns the remainder): %%
- Integer division: %/%

Notably, assignment operations in R are written as ```variable <- value``` rather than a single equal sign.

There are also logical operators and comparisons:
- Equal-to: ==
- Not-equal-to: !=
- Less-than: <
- Greater-than: >
- Less-than or equal-to: <=
- Greater-than or equal-to: >=
- AND (both are TRUE): &
- OR (at least one is TRUE): |

(Interactive examples of all in PLP2.Rmd)


## PLP 3 - Functions

### Declaring a function in R
The syntax to declare a function is <yourFunctionName <- function(parameters) {definition}>. Functions must be declared before (above) they are called in the code. R does not allow functions to return more than one value, but it does support the ability to pass multiple parameters of different types into a function (PLP3.Rmd: multitype). It also allows recursive (self-calling) functions (PLP3.Rmd: factfunct).

### Pass-by-reference or pass-by-value?
Whether a language is "pass-by-reference" or "pass-by-value" determines what happens when you assign a variable to another variable. Depending on the language's design, it may copy the value of the old variable into the new one (pass-by-value) or it may create the new variable as an alias of the old variable that will reflect any changes that occur to it (pass-by-reference). We can tell which protocol a language uses by assigning an old variable to a new variable, changing the value of the old variable, and then checking the value of the new variable. If the new value changed with the old variable, the language is pass-by-reference. If the new variable holds the value that the old variable initially started with, it is pass-by-value. As you can see in the PLP3.Rmd example "new/old", R is a pass-by-value language.




