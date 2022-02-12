# Matching a Hex Value

Regular Expressions (Regex) are sequences of characters that define a search pattern, mainly for use in pattern matching with strings, or string matching. Regexes are a generalized way to match patterns with sequences of characters. (geeksforgeeks.org/write-regular-expressions)

## Summary

In this tutorial, we will be covering the components of a regex used to match a hex value. Hexadecimal code is used to describe a color using a # key followed by six digits of code. That value is used to define a color with consistency and accuracy to be used as a universal code for any given color. /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

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

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

Note: As the Regex is considered a literal, the pattern must be wrapped in / at the beginning and end.

### Anchors

/`^`#?([a-f0-9]{6}|[a-f0-9]{3})`$`/

The characters `^` and `$` are both considered to be the anchors in the above expression. The `^` anchor marks the start of the string of characters that can be included. 

The `$` at the end of the string marks that all the characters before it can be used. In other words, `^` characters that can be used `$`. 

With that information in mind, we can conclude that the information after the `^` and before the `$` is #?([a-f0-9]{6}|[a-f0-9]{3}). Those are the characters that can be included in the expression.

### Quantifiers

/^#`?`([a-f0-9]`{6}`|[a-f0-9]`{3}`)$/

A quantifier sets the limits of the string your regex matches. They will typically contain the minimum and maximum number of characters that your regex is looking for. In our expression, the `?` that the pattern must be matched zero or one time. Other quantifiers `*+` or `{}`. Quantifiers are inherently greedy. This means that they will match as many occurrences as possible of a given pattern unless they are limited by the characters previously mentioned.

The {} contain a number inside. That number sets the limits of how many characters can be included in the string. For example, `{6}` means that there must be 6 characters in the string while `{3}` means that there must be 3 characters. If the expression contaned a `{ 3, 6 }`, that would mean minimum of `3`, maximum of `6`.

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

My name is Jason Boudreaux. I am a Full Stack Web Development Boot Camp student at SMU.
GitHub profile: github.com/jsnbdrx