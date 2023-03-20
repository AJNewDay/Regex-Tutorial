# Tutorial for Using Regex Expressions

Regex expressions are useful tools that assist developers in locating specific types of data within large fields of text or code. We can use regex expressions to find just about anything that may be present within the files we are searching. Practical examples of this could be email addresses, phone numbers, URL's, and specifc strings of data.

## Summary

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

For this example we'll be looking at the expression provided above and seeing how it is used to match an email address.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

The anchors of Regex expressions are the ^ and $ symbols. They tell the program where to begin and stop searching for matches within the data. The ^ will always be placed at the beginning and the $ will always be at the end.

### Quantifiers

Quantifiers can be represented by the symbols, \*, +, ?, or {}. The quantifiers at use in our example would be +, and {2,6}.
The + symbol tells us that the sets of characters being searched for must be matched at least 1 time. The expression {2,6} allows for matches of the carachters it is searching for between 2 and 6 times.

### Grouping Constructs

Grouping Constructs allow us to break up the expression we are using into "sub-expressions". These sub-expressions might be represented by names, titles, or other strings of data. Grouping constructs are represented by characters surrounded by parentheses.
The sub-expessions present in our example are ([a-z0-9_\.-]+), ([\da-z\.-]+), and ([a-z\.]{2,6}).

### Bracket Expressions

Bracket Expressions are used to match characters found within the expression's square brackets. [a-z0-9_\.-], [\da-z\.-], and [a-z\.]. The bracket expressions we're looking at here will indicate which character groups will create a match when the expression is run. "a-z" will look for single, lowercase, alphabetic characters ranging from a to z. "0-9" searches for single, numeric characters ranging from zero to nine. "\_\.-" is going to match the underscore and hyphen symbols. "\da-z\.-" will match digits with a value range of zero to nine, lowercase alphabetic characters from a to z, and the dot character. And lastly the "a-z\." expression will find lowercase alphabetic characters followed by a "."

### Character Classes

Character Classes are used in order to find matches within different types of character sets. Examples can be the digit class, inverse classes, and the dot class. As we saw in the example of bracket expressions above, "\d" is a digit class that allows us to match numeric symbols.

### The OR Operator

The OR Operator, also referred to as "Alternation", is represented by the vertical line symbol, "|". It enables us to match characters within a range of parameters that we determine for ourselves. Our current Regex example does not contain this operator.

### Flags

Using flags in our regex expressions lets us alter the way in which the expression performs its search. Javascript utilizes six regex flags represented by the characters, "i" to perform a search that is case insensitive, "g" to search for global instances of the expression, "s" to make the dot character search in new lines, "m" to make the anchors search for matches on every line, "y" uses the lastIndex property as the launch point for new searches, and "u" to include 32-bit characters in its search. Our current example does not contain any flags.

### Character Escapes

Character escapes are a way for us to enforce the literal interpretation of characters. This is accomplished by placing a backslash in front of a character that we want the expression to match rather than use as a quantifier or grouping mechanism. the "\." example in our expression "escapes" the dot's normal function of matching all characters and simply looks for a literal "."

## Author

Written by Aaron Jordan on March 20th, 2023

https://github.com/AJNewDay/Regex-Tutorial
