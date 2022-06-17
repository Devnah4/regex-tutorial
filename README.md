# Regex Tutorial

This is a simple tutorial on REGEX demonstrating some of the terms with examples.

Examples of affected code will be *italicized*

## Summary

The code I will be using is to verify wheter an email has been input correctly

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

__ANCHORS__ are components used to match either starting strings (^) or the end of a string ($).

```
^General
```
This would match any string that starts with *General*  

```
Kenobi$
```
This would match any string that ends with *Kenobi* 

```
^General Kenobi$
```
This would match any string that starts with __General__ and ends with __Kenobi__

### Quantifiers

__Quantifiers__ are used to search for set amount of characters after an initial value using (*, +, ?, {})

```
Darth+
```
This would match the value for any value that had Dart with a value of h at 1 or higher.

example:

*Darth* / *Darthhhh* / Dart 


```
Darth{2,6}
```
This would match the value for Dart and then values of H from 2 until 6.

example:

Darth / *Darthhhh* / Darthhhhhhh

### OR Operator

__OR__ operators are used to match a string with content right after it

```
ig-[\d]
```
This will match a single digit right after the previous string

Example: 

*ig-8*8 / *ig-9*01 / ig88

### Character Classes

__Charcter Classes__ match the data with specific constructs using (\d, \w, \s, .)

```
O\d\d
```

using \d will match to any digit [0-9]

Example: 

*O66* / O6 / O123

```
A\w\w
```

using \d will match to any alphabetical character [a-z] and underscores

Example: 

*ABC* / *A_C* / 123

```
O\s\s
```

using \d will match to any whitespace

Example: 

*O__* / O6 / O123

### Flags

__Flags__ are used to denote the begining and end of the regex operator and are denoted as (/)

```
/\d\d\d/
```
This will simply pull 3 digits

example:

*123* / *345* / abc

### Grouping and Capturing

__Grouping__ allows the user to set a specific grouping of charcaters in parenthesis [()]. This is useful when neededing to pull specific data

```
(abc)(123)
```
This will pull the value for abc and 123 as 2 seperate finds meaning you could use either value

### Bracket Expressions

__Bracket Expression__ uses ([]) in the same way as an array allowing the user to pull each item in the array individually. 

```
[han, solo]
```
This notation would allow you to pull all the characters in han and solo allowing you find close to or similair values as well

Example:

*han solo* / *l*uke *s*kyw*al*ker

### Greedy and Lazy Match

__Greedy__ matches pull as much info as they can from a string

example:

```
<.+>
```
This will catch anything between (<>) results

```
<p>Han shot first</p>
```
This will return everything from the first < to the last >.

__Lazy__ matches fix this by telling it to ONLY grab the specific piece it is looking for

 ```
 <.+?>
 ```
 ```
 <p>Han shot first</p>
 ```
 With this code snippet it will only return what is in the (<>) brackets which would be p and /p
 
### Boundaries

__Boundaries__ are similair to anchors exept they look outside of the search term using (\b or \B)

```
\blightsaber\b
```
using this syntax you'd be able to find just the word lightsaber in a sentence.

```
\Bsaber\b
```

Using this syntax however would find the word saber within lightsaber using the /B to notate something would be before it

### Back-references

__Back Refrences__ use the syntax (\[1]) to match the same text that was in the first capture group

```
[123]\1
```
using this syntax we can check for doubles for example 11, 22, 33

## Author

Hi there! my name is Martin and i'm a beginner coder. Check out my [GitHub](https://github.com/Devnah4) to see some of my work.
