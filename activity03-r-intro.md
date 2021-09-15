Activity 3
================
Hudson Ruhlig

You will be creating and manipulating vectors, lists, and data frames to
uncover a top secret message.

As you work through this document with your Team members, remember to:

-   Ask questions
-   Google is your friend! If an error is confusing, copy it into Google
    and see what other people are saying. If you don’t know how to do
    something, search for it.
-   Just because there is no error message doesn’t mean everything went
    smoothly. Use the console to check each step and make sure you have
    accomplished what you wanted to accomplish.

Do not edit this first R code chunk. This will allow you to knit your
document and view errors within the knitted report.

### Setup

Each of the following R chunks will cause an error and/or do the desired
task incorrectly. Find the mistake, and correct it to complete the
intended action.

Create three vectors that contain: 1) the lower case letters, 2) the
lower case letters, and 3) some punctuation marks.

``` r
lower_case <- c("a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z")

upper_case <- c("A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z")

punctuation <- c(".", ",", "!", "?", "'", '"', "(", ")", " ", "-", ";", ":")
```

Comment on what you noticed about the errors and how you used this
information to correct the issues.

**Response**:

Using the errors stating there were unexpected string constants in
specific arguments. In the arguments for the vectors, there were
punctuation issues that were changed to fix the errors and complete the
vectors.

Make one long vector containing all the symbols.

``` r
my_symbols <- c(lower_case, upper_case, punctuation)
my_symbols
```

    ##  [1] "a"  "b"  "c"  "d"  "e"  "f"  "g"  "h"  "i"  "j"  "k"  "l"  "m"  "n"  "o" 
    ## [16] "p"  "q"  "r"  "s"  "t"  "u"  "v"  "w"  "x"  "y"  "z"  "A"  "B"  "C"  "D" 
    ## [31] "E"  "F"  "G"  "H"  "I"  "J"  "K"  "L"  "M"  "N"  "O"  "P"  "Q"  "R"  "S" 
    ## [46] "T"  "U"  "V"  "W"  "X"  "Y"  "Z"  "."  ","  "!"  "?"  "'"  "\"" "("  ")" 
    ## [61] " "  "-"  ";"  ":"

Comment on what you noticed about the errors and how you used this
information to correct the issues.

**Response**:

Using the error I noticed that the function cbind() was not the proper
function for creating simple vectors with the other created vectors.
Looking at the created vectors above, I changed the function to properly
create the my\_symbols function.

Turn the `my_symbols` vector into a data frame, with the variable name
“Symbol”.

``` r
my_symbols <- data.frame(my_symbols)
names(my_symbols) <- "Symbol"
my_symbols
```

    ##    Symbol
    ## 1       a
    ## 2       b
    ## 3       c
    ## 4       d
    ## 5       e
    ## 6       f
    ## 7       g
    ## 8       h
    ## 9       i
    ## 10      j
    ## 11      k
    ## 12      l
    ## 13      m
    ## 14      n
    ## 15      o
    ## 16      p
    ## 17      q
    ## 18      r
    ## 19      s
    ## 20      t
    ## 21      u
    ## 22      v
    ## 23      w
    ## 24      x
    ## 25      y
    ## 26      z
    ## 27      A
    ## 28      B
    ## 29      C
    ## 30      D
    ## 31      E
    ## 32      F
    ## 33      G
    ## 34      H
    ## 35      I
    ## 36      J
    ## 37      K
    ## 38      L
    ## 39      M
    ## 40      N
    ## 41      O
    ## 42      P
    ## 43      Q
    ## 44      R
    ## 45      S
    ## 46      T
    ## 47      U
    ## 48      V
    ## 49      W
    ## 50      X
    ## 51      Y
    ## 52      Z
    ## 53      .
    ## 54      ,
    ## 55      !
    ## 56      ?
    ## 57      '
    ## 58      "
    ## 59      (
    ## 60      )
    ## 61       
    ## 62      -
    ## 63      ;
    ## 64      :

Comment on what you noticed about the errors and how you used this
information to correct the issues.

**Response**:

In the errors, I noticed there was punction issues with the data.frame()
function, and missing quotations in the naming assignment of the created
data frame.

Find the total number of symbols we have in our data frame.

``` r
len <- nrow(my_symbols)
len
```

    ## [1] 64

Comment on what you noticed about the errors and how you used this
information to correct the issues.

**Response**: I noticed that the function length() wasn’t working so I
used the internet to find the proper function for counting rows of a
vector

5.  Create a new variable in your dataframe that assigns a number to
    each symbol.

``` r
my_symbols$Num <- 1:len
my_symbols
```

    ##    Symbol Num
    ## 1       a   1
    ## 2       b   2
    ## 3       c   3
    ## 4       d   4
    ## 5       e   5
    ## 6       f   6
    ## 7       g   7
    ## 8       h   8
    ## 9       i   9
    ## 10      j  10
    ## 11      k  11
    ## 12      l  12
    ## 13      m  13
    ## 14      n  14
    ## 15      o  15
    ## 16      p  16
    ## 17      q  17
    ## 18      r  18
    ## 19      s  19
    ## 20      t  20
    ## 21      u  21
    ## 22      v  22
    ## 23      w  23
    ## 24      x  24
    ## 25      y  25
    ## 26      z  26
    ## 27      A  27
    ## 28      B  28
    ## 29      C  29
    ## 30      D  30
    ## 31      E  31
    ## 32      F  32
    ## 33      G  33
    ## 34      H  34
    ## 35      I  35
    ## 36      J  36
    ## 37      K  37
    ## 38      L  38
    ## 39      M  39
    ## 40      N  40
    ## 41      O  41
    ## 42      P  42
    ## 43      Q  43
    ## 44      R  44
    ## 45      S  45
    ## 46      T  46
    ## 47      U  47
    ## 48      V  48
    ## 49      W  49
    ## 50      X  50
    ## 51      Y  51
    ## 52      Z  52
    ## 53      .  53
    ## 54      ,  54
    ## 55      !  55
    ## 56      ?  56
    ## 57      '  57
    ## 58      "  58
    ## 59      (  59
    ## 60      )  60
    ## 61         61
    ## 62      -  62
    ## 63      ;  63
    ## 64      :  64

Comment on what you noticed about the errors and how you used this
information to correct the issues.

**Response**:

I used the shorthand to access new variables with the $

![](README-img/noun_pause.png) **Planned Pause Point**: If things made
sense, feel free to continue on while you wait. Otherwise, contact your
instructor to have them verify your work.

### Decoding the secret message.

This chunk will load up the encoded secret message data and assign it as
a vector. There are no errors here.

``` r
# Read in full csv file
top_secret <- readr::read_csv("data/secret_code.csv", col_names = FALSE)
```

    ## 
    ## ── Column specification ────────────────────────────────────────────────────────
    ## cols(
    ##   X1 = col_double()
    ## )

``` r
# Pick off only the column X1
top_secret <- top_secret$X1
```

By altering this top secret set of numbers, you will be able to create a
message. Write your own code to complete the steps below.

1.  Add 14 to every number.
2.  Multiply every number by 18, then subtract 257.
3.  Exponentiate every number. (That is, do e ^ \[each number\]. You may
    need to Google how to this!)
4.  Square every number.

**HQ UPDATE:** Headquarters has informed you that at this stage of
decoding, there should be 496 numbers in the secret message that are
below 17.

5.  Turn your vector of numbers into a matrix with 5 columns.
6.  Separately from your top secret numbers, create a vector of all the
    even numbers between 1 and 502. Name it “`evens`”. That is, `evens`
    should be an R object that contain the values 2, 4, 6, 8, …, 502.
7.  Subtract the “evens” vector from the first column of your secret
    message matrix.
8.  Subtract 100 from all numbers 18-24th rows of the 3rd column.
9.  Multiply all numbers in the 4th and 5th column by 2.
10. Turn your matrix back into a vector.

**HQ UPDATE:** Headquarters has informed you that at this stage of
decoding, all numbers in indices 500 and beyond are below 100.

11. Take the square root of all numbers in indices 38 to 465.
12. Round all numbers to the nearest whole number.
13. Replace all instances of the number 39 with 20.

**HQ UPDATE:** Headquarters has informed you that your final message
should have 421 even numbers.

![](README-img/noun_pause.png) **Planned Pause Point**: If things made
sense, feel free to continue on while you wait. Otherwise, contact your
instructor to have them verify your work.

## The secret message!

Use your final vector of numbers as indices for `my_symbols` to discover
the final message, by running the following code:

``` r
stringr::str_c(my_symbols$Symbol[top_secret], collapse = "")
```

    ## [1] ""

Google the first line of this message, if you do not recognize it, to
see what it is.

**delete this line and comment on what on the activity as a whole**

Comment on what you noticed about the activity as a whole.

**Response**:

Push your updated report to your `<username>` branch - you are done with
this `.Rmd` file and can go back to the README directions while you wait
for you Team Members.

## Attribution

This activity is based on a lab from [Dr. Kelly
Bodwin](https://www.kelly-bodwin.com/)’s Stat 331 course
