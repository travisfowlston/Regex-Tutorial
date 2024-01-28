# Regex Tutorial

A regex, which is short for regular expression, is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input. The Module 17 Challenge objective was to create a tutorial that explains how a specific regular expression, or regex, functions by breaking down each part of the expression and describing what it does.

## Summary

In this tutorial, I will be breaking down and describing what the Matching an Email – `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` regular expression is doing. To achieve this, I will begin by explaining the anchors and specifically how they start and end the expression. Then I will explain each of the three components of this expression to show how this is ultimately used to match an email address.

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

For reference, this is the expression: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

### Anchors

The anchors are the symbols that start and end the regular expression. In this case, the beginning anchor is the ^ symbol. It signifies the beginning of a string with all of the characters that come after it. The $ symbol is used to signify the end the of string. Therefore, everything in between the ^ symbol and the $ symbol must meet this criteria: `([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`.

### Quantifiers

Quantifiers are the set limits of the string that the regular expression can match. These typically include a minimum and maximum number of characters that the string can include. This is shown in the last component of our expression, `{2,6}`. In this, because it is grouped together with `[a-z\.]`, it is setting the minimum number of two characters and the maximum number of six characters for this grouping. the + symbol is also a quantifier but I will talk about that more in the Greedy and Lazy Match section.

### Bracket Expressions

The brackets, [], represent the the range of the characters that we want to match. In the code snippet `[a-z0-9_\.-]`, everything within the brackets is what we want to include. The `[a-z]` represents that the string cantain the lowercase letters a through z. The `[0-9]` represents that the string can contain any number between 0 and 9. The `[_\.-]` represent that the string can contain an underscore, dot, and hyphen. In summary, the bracket expressions `[a-z0-9_\.-]`, `[\da-z\.-]`, and `[a-z\.]` are used to match specific sets of characters.

### Character Classes

A character class defines a set of characters which can occur in an input to fulfill a match. The above bracket expressions are considered character classes. The only character class that isn't defined from above is the use of the `\d` from the second component of the expression. `\d` matches any Arabic numeral digit. It is equivalent to the bracket expression `[0-9]`.

### Grouping and Capturing

### Greedy and Lazy Match

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
