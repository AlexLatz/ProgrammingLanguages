
# AlphaLang Cversion Zero One OneD

## The programming language with only letters

This language was developed by Alex Latz in two thousand twenty two
in Honors Programming Languages at The Westminster Schools.

However, instead of some *lesser* non-numerical languages,
Alpha focuses on pure WPM.
Alpha's goal is to allow even faster programming with a
modified and improved C style syntax.

Due to this focus, Alpha uses a large number of reserved symbols and
almost all uppercase letters. We call this style **platypuscase**.

![Flat Platypus](https://www.nhm.ac.uk/content/dam/nhmwww/discover/platypus-puzzle/platypus-full-width.jpg.thumb.1160.1160.jpg)

## Basic Syntax

### Line Endings

Most symbols have a one-to-one replacement in Alpha. One notable exception is the semicolon, as statements in Alpha are generally finished with a newline character.
However, statements in Alpha can be multi-line with the use of an indent.

Additionally, a line can be intentionally ended with the O character.

ex. 
```
let name be one X
    two
let nametwo be two X one
let namethree be two X three O
```

### Creating Scope

All scope in Alpha is separated by the `L` and `J` characters, instead of `{}` in C. 
Additionally, all functions and statements that usually require the `()` parentheses are replaced by `C` and `D`.
ex. 
```
if Cone is twoD L
    rtrn false
J
```

### Comments

Comments in Alpha can be at any point within a line of code. 
Comments are indicated with the `II` symbol.

```
let var be five II comment
II comment two
```


## Variables

### Initialization

Alpha is a weakly typed language with soft initialization.
This means that all variables are declared with the same syntax and can be shifted between types.
All variables are declared with the keyword `let` and optionally initialized with the keyword `be` (where `be` is equal to `=` in C-style).

```
let tmp be true  
let name be twenty five point one
let var
```

Negative numbers are declared with the `zero sub` prefix.
ex. `zero sub one is zero sub one`

### Modification

Variables can be modified later through the `be` keyword.

### Strings and Chars

Strings in Alpha are declared between `dB` and `Db` symbols, and must be separated from their endings by a space character on either end.
Additional spaces will be incorporated into the string.

Chars follow the same rules, except for the `cB` and `Cb` delimiters before and after the char. `In` is equivalent to the newline char. 

ex. 
```
let name be dB Hello, World! Db
let chr be cB In Cb
let blank be dB  Db II important: two spaces in between
```

## Functions

Functions can be declared using the `fxn` keyword. To provide arguments to a function, enclose a space-separated list of variable names with `CD`.

Multi-parameter functions must separate each parameter with the `I` delimiter character. 
```
fxn squareCxD L
    rtrn x X x
J
fxn addThreeCaI bI cD L
    rtrn a add b add c
J
squareCfiveD
addThreeConeI twoI threeD
```

### Printing

Alpha uses the `printCD` function to print output to the console, and the `printlnCD` function to print with a newline character appended after the input.

You can pass multiple values into either function, and it will print each parameter Cwith a newline appended each time for printlnD.

## Operators

Alpha's operators are fairly different from most languages.

| Operator |        Behavior         | Usage                                  |
|:--------:|:-----------------------:|:---------------------------------------|
|   `be`   |       Assignment        | `varname be two`                       |
|  `add`   |        Addition         | `one add two`                          |
|  `sub`   |       Subtraction       | `two sub one`                          |
|   `X`    |     Multiplication      | `one X two`                            |
|  `div`   |        Division         | `two div one`                          |
|  `mod`   |         Modulo          | `two mod one`                          |
| `addbe`  |       Plus-equals       | `var addbe one`                        |
| `subbe`  |      Minus-equals       | `var subbe one`                        |
|  `Xbe`   |      Times-equals       | `var Xbe one`                          |
| `divbe`  |      Divide-equals      | `var divbe one`                        |
| `modbe`  |      Modulo-equals      | `var modbe one`                        |
|  `inc`   |        Increment        | `var inc`                              |
|  `dec`   |        Decrement        | `var dec`                              |
|  `less`  |       Lesser than       | `var less vartwo`                      |
|  `more`  |        More than        | `var more vartwo`                      |
|   `is`   |        Equal to         | `var is vartwo`                        |
| `lessis` | Lesser than or equal to | `var lessis vartwo`                    |
| `moreis` |  More than or equal to  | `var moreis vartwo`                    |
|  `not`   |       Logical NOT       | `not Cvar is vartwoD`                  |
|  `and`   |       Logical AND       | `var is vartwo and vartwo is varthree` |
|   `or`   |       Logical OR        | `var is vartwo or vartwo is varthree`  |

## Conditionals

Unlike the operators, conditionals in Alpha are mostly similar to C-style.

`if` statements can be followed with `elif` or `else` and are followed by `CD` with a conditional inside. 

```
if Cvar is oneD L
    II do something
J elif Cvar is twoD L
    II do something
J else L
    II do something
J
```

## Looping

Alpha supports for and while loops.

| Behavior | Example                                    |
|:--------:|:-------------------------------------------|
| For loop | `for Clet i be one O i less five O i incD` |
|  While   | `while Cvar lessis vartwoD`                |


### Cross-Type Operations

A full list of operators and their results for different types can be found [here](https://docs.google.com/spreadsheets/d/1QlgnHaIWgfmdPA5GC0O03QBLwU0wPlMuLVbpba64jYk/edit?usp=sharing).
