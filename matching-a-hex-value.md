# Matching a Hex Value

Regular Expressions (Regex) are sequences of characters that define a search pattern, mainly for use in pattern matching with strings, or string matching. Regexes are a generalized way to match patterns with sequences of characters.

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

/^#?([a-f0-9]{6} `|` [a-f0-9]{3})$/

The OR operator is marked by the `|` character. We might have noticed that our expression has {6} and {3} in it. How could it be 6 characters AND 3 characters at the same time? Enter the OR Operator. This separates our expression into two parts. This shows that we can have the expression as a 6 character string OR `|` a 3 character string. 

### Character Classes

/^#?([`a-f`0-9`]{6}|[`a-f``0-9`]{3})$/

A character class in a regex defines a set of characters. Any of the mentined characters can be used in the string. In our example, `a-f` and `0-9` are the two character classes. This signifies that the letters abcdef and numbers 0 1 2 3 4 5 6 7 8 and 9 are all able to be used in the string. Examples of accepted strings based on this criteria are: #000fe5, #ffff12, and #abc123. However these strings would not be accepted based on this criteria: #000jkl, #uafwef. Those two strings contain letters that are not within the `a-f` parameter. 

### Flags

A flag would be placed in a regex at the end, after the final `/`. It would define an additional functionality or limit for the regex. There are 7 flags that can be used.
* g - global search
* i - case-insensitive search
* m - multi-line search
* d - generate indices for substring matches
* s - allows . to match newline characters
* u - treat a pattern as a sequence of unicode code points
* y - sticky search that matches starting at the current position in the target string

No flags are used in our expresion.

### Grouping and Capturing

/^#?`(`[a-f0-9]{6}|[a-f0-9]{3}`)`$/

The primary way to group a section of a regex is by using `()`. Each section withing `()` is known as a subexpression. In our example, we have one group construct: [a-f0-9]{6}|[a-f0-9]{3}. 

### Bracket Expressions

/^#?(`[a-f0-9]`{6}|`[a-f0-9]`{3})$/

A bracket expression is used distinguish which characters are able to be used in the expression. In our example, our bracket expression indicates that we can use letters `a-f` and/or numbers `0-9`. The expression distinguishes the two types of characters that can be used.

### Greedy and Lazy Match

/^#`?`([a-f0-9]{6}|[a-f0-9]{3})$/

A greedy match tries to match an element as much as possible while a lazy match tries to match an element as few times as possible. Our example has a `?` after the `#` symbol. This is a greedy match. The `?` indicates that the expression can use the `#` 0 or 1 time.  

## Author

My name is Jason Boudreaux. I am a Full Stack Web Development Boot Camp student at SMU.
[GitHub profile](github.com/jsnbdrx)