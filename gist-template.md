# Title (RegEx)

Regex is a powerful tool that allows us to efficiently search for and replace characters or strings by utilizing metacharacters. It consists of a string of metacharacters that define a specific search pattern.

In this tutorial, the focus is on a regex string designed to identify dates in the format dd-MM-YYYY. Our regex string is comprised of three distinct sub-strings combined with an OR operator ( | ), each targeting the day, month, and year separately. Below is the code.
## Summary
This tutorial specifically focuses on the following regex used to find dates in the format of dd-MM-YYYY:. This regex is composed of 3 strings, joined with an OR operator ( | ), and they are separated out below in the code snippet.

The three strings look for each component in the date format - day, month, and year.
```
^(?:(?:31(\/|-|\.)(?:0?[13578]|1[02]))\1|(?:(?:29|30)(\/|-|\.)(?:0?[1,3-9]|1[0-2])\2))(?:(?:1[6-9]|[2-9]\d)?\d{2})$|


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
- This Regex is composed of the following components:
 - Character Classes - specific sets of characters used in the search.
 - Anchors - find the starting and ending points of a string.
 - Escaping Characters - can be used to insert special, reversed, and unicode characters.
 - Groups & References - match a pattern multiple times within a string.
 - Quantifiers & Alternation - specify how many characters should match.

### Anchors
 - Anchors are used to identify the beginning and end of the string.
 - Our entire regex string is actually composed of 3 different strings - one for the day, month, and year respectively - and they are all wrapped with the following opening and closing anchors:
 - Opening Anchor: ```^```
 - Closing Anchor: ```$```

### Quantifiers
- Specifies how many of the preceeding character/token should be matched.
- Examples from our strings:
    - ```?``` - match between 0 and 1 of the preceding token.
    - ```{2}``` - match 2 of the preceding token.
### Grouping Constructs
- Grouping can be used as a non-capture group or capture group. 
- Non-capture Group - groups up multiple tokens without creating a capture group. In our examples, these are typically nested within eachother, with a capture group also nested inside:
    - ``` (?:(?:31(\/|-|\.)(?:0?[13578]|1[02]))\1|(?:(?:29|30)(\/|-|\.)(?:0?[1,3-9]|1[0-2])\2)) ```
    - ``` (?:31(\/|-|\.)(?:0?[13578]|1[02])) ```

- Capture Group - groups multiple token for extracting: 
    - ```(\/|-|\.) ```
### Bracket Expressions
- A bracket expression is either a matching list expression or a non-matching list expression.
- It consists of one or more expressions: ordinary characters, collating elements, collating symbols, equivalence classes, character classes, or range expressions.

### Character Classes
- Matches a character from a specific set. All of our character classes in our strings consist of numbers.
- Examples:
    - ```[13578]```
    - ```[02]```
    - ```[1,3-9]```
    - ```[0-2]```
    - ```[6-9]```
 
### The OR Operator
- Defined as a vertical slash ```|```
- Matches the expression before or after the ```|```
- The easiest examples are the vertical slashes which join all of our strings together - which are the vertical slashed coming before the ```^```
- Many other examples within the grouping constructs
### Flags
- A regular expression consists of a pattern and optional flags: g, i, m, u, s, y.
- Without flags and special symbols (that we’ll study later), the search by a regexp is the same as a substring search.
- The method str.match(regexp) looks for matches: all of them if there’s g flag, otherwise, only the first one.
- The method str.replace(regexp, replacement) replaces matches found using regexp with replacement: all of them if there’s g flag, otherwise only the first one.
- The method regexp.test(str) returns true if there’s at least one match, otherwise, it returns false.
### Character Escapes
- A character escape represents a character that may not be able to be conveniently represented in its literal form.
-examples
    -\f, \n, \r, \t, \v
    -\cA, \cB, …, \cz
    -\u{HHH}
## Author

My name is roberto and a novice programmer in front end and backend programming (https://github.com/rm2023)
