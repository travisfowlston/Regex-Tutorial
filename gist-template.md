# Regex Tutorial

A regex, which is short for regular expression, is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input. The Module 17 Challenge objective was to create a tutorial that explains how a specific regular expression, or regex, functions by breaking down each part of the expression and describing what it does.

## Summary

In this tutorial, I will be breaking down and describing what the Matching an Email – `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` regular expression is doing. To achieve this, I will begin by explaining the anchors and specifically how they start and end the expression. Then I will explain each of the three components of this expression to show how this is ultimately used to match an email address.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Author](#author)

## Regex Components

For reference, this is the expression: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

### Anchors

The anchors are the symbols that start and end the regular expression. In this case, the beginning anchor is the "^" symbol. It signifies the beginning of a string with all of the characters that come after it. The "$" symbol is used to signify the end the of string. Therefore, everything in between the "^" symbol and the "$" symbol must meet this criteria: `([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`.

### Quantifiers

Quantifiers are the set limits of the string that the regular expression can match. These typically include a minimum and maximum number of characters that the string can include. This is shown in the last component of our expression, `{2,6}`. In this, because it is grouped together with `[a-z\.]`, it is setting the minimum number of two characters and the maximum number of six characters for this grouping. The "+" symbol is also a quantifier and is inherently greedy. That means it matches one or more occurrences of the element that preceeds it. In our example, the "+" symbol is used to match one or more occurrences of the braket expressions that preceed it.

### Bracket Expressions

The brackets, [], represent the the range of the characters that we want to match. In the code snippet `[a-z0-9_\.-]`, everything within the brackets is what we want to include. The `[a-z]` represents that the string cantain the lowercase letters a through z. The `[0-9]` represents that the string can contain any number between 0 and 9. The `[_\.-]` represent that the string can contain an underscore, dot, and hyphen. In summary, the bracket expressions `[a-z0-9_\.-]`, `[\da-z\.-]`, and `[a-z\.]` are used to match specific sets of characters. I will dive deeper into what each component is doing in the Grouping and Capturing section.

### Character Classes

A character class defines a set of characters which can occur in an input to fulfill a match. The above bracket expressions are considered character classes. The only character class that isn't defined from above is the use of the `\d` from the second component of the expression. `\d` matches any Arabic numeral digit. It is equivalent to the bracket expression `[0-9]`.

### Grouping and Capturing

Grouping is when you use parentheses, "()", to group together characters or subexpressions to create a single unit. I have been referring to these as components. Combining all the logic I have stated in the other sections, we can determine that the first component `([a-z0-9_\.-]+)`, matches one or more lowercase letters, digits, underscores, dots, or hyphens. This is representing the username part of the email address. Then, the "@" symbol that follows is matched literally. The second component `([\da-z\.-]+)`, matches one or more digits, lowercase letters, dots, or hyphens. This is representing the domain name part of the email address. The `\.` matches the literal dot symbol, which separates the domain name from the top-level domain. The third component `([a-z\.]{2,6})`, matches two to six lowercase letters or dots. This is representing the top-level domain part of the email address. Finally, combining these three components ensures that the email address follows a specific pattern with a username, an "@" symbol, a domain name, and a top-level domain.

## Author

Hi there! My name is Travis Fowlston, and I'm a dedicated full-stack web developer who thrives on exploring new technologies and sharing my knowledge with the web development community. With a background in web development, I specialize in creating full-stack applications. Throughout this boot camp, I have honed my skills in HTML, CSS, JavaScript, and various front-end frameworks like React. On the back-end, I have expertise in Node.js, Express, and working with databases such as MongoDB and MySQL. I have a particular interest in developing interactive and user-friendly web applications. I enjoy tackling projects that require both creative problem-solving and technical implementation. I am always eager to learn new technologies and keep up with the latest industry trends.

### GitHub Profile

You can find more about my work and projects on my [GitHub profile](https://github.com/travisfowlston)

Feel free to reach out to me if you have any questions or if you'd like to collaborate on any exciting projects!
