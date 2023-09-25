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
#Anything I write here is for humans to read!
print("This is a sample line of code") #And over here
#And over here too!

# And all these lines
# are "commented out"
# as well :)
```

For multi-line comments (for example, a block of code you want to temporarily hide from your program), highlight the section and use the command "ctrl + shift + c"
