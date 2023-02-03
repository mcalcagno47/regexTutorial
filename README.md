# REGEX Tutorial: Matching an email


## Introduction

The purpose of this tutorial is to break down an example of a Regular Expression, or REGEX.  The specific expression described in this lesson is used to match an email, which looks like this: 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

Throughout this document, I will separate the sections of this expression into its core components and explain their functions.  It is the hope of this amateur web-developer that it will be a useful resource for not only myself, but others who need help deciphering Regular Expressions.


## Summary

This code is meant to check an email address amongst others in the database for the purpose of matching, locating and managing it.  There are three sections to an email address: the unique handle that can contain letters, numbers and symbols, the @ symbol that separates the handle from the email client (which can be numerals or letters), and the domain, which is preceded by a period and can be between 2 and 6 lowercase letters long.


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
The following anchors are present in the above expression: 
^ at the beginning begins the string
$ at the end of the expression ends the string

### Quantifiers
The following quantifiers are present in the above expression:
+ allows for 1 or more characters to be used
{2,6} means that in the domain section can only be between 2 and 6 characters long

### Grouping Constructs
() are used to capture groups of characters. Character groups are placed within them, signified with [].
[] are used to begin and end character groups.  See Bracket Expressions. 


### Bracket Expressions
The characters within brackets define the rules of a character group.

[a-z0-9_\.-] means letters, numbers and dashes can be used in the unique identifier.

[\da-z\.-] means letters in English and other languages can be recognized in the email client

[a-z\.] means letters can  be used in the domain, though these are limited by the quantifier {2,6}.  See the Quantifiers section above.


### Character Escapes
\.- is seen a number of times in the expression.  Its purpose is to disambiguate the language element “-“, allowing the expression to use that specific symbol in the string of characters, and not be confused for the other meaning of that symbol in the context of Regular Expressions.  Dashes can be used in any of the sections of an email address, but other symbols cannot.  These escapes allow for this to occur.  Since symbols like the underscore have no other meaning in REGEX, it is not necessary to disambiguate them.


## Author

Mark Calcagno
GitHub: https://github.com/mcalcagno47 

