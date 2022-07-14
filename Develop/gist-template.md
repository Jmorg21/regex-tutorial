# Tutorial: Regex Matching an Email

Regex is shorthand for "Regular Expression", which is a pattern that developers can use to replace objects within a string while writing JavaScript.

## Summary

This regex can be used to verify that an object is an email address:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

While this may look like gibberish now, read on to understand how this seemingly random group of characters can be an extremely helpful tool while writing your script!

## Table of Contents

- [Tutorial: Matching an Email with Regex](#tutorial-matching-email-with-regex)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [Character Classes](#character-classes)
    - [Grouping and Capturing](#grouping-and-capturing)
    - [Bracket Expressions](#bracket-expressions)
    - [Greedy and Lazy Match](#greedy-and-lazy-match)
  - [Author](#author)

## Regex Components

A Regex is made made up of several components. While it may look like complete gibberish, it can be better understood when you break it down into smaller components. The regex we are using as an example is: "/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/". This Regex can be broken down into these components:

### Anchors

The Anchors found in this expression are "^", and "$". Anchors don't match other characters, rather they match a position before or after the other experession characters. They are used to "anchor" the regex as the first and last components. In our example the "^" matches the position before the first character as you can see: /^([a-z0-9_\.-]+. The "$" matches right after the last character in our example.

### Quantifiers

As the name may suggest, quantifiers specify how many of a character, or group of characters must be present for a match to be found. Quantifiers are often found between two curly braces, such as "{a,b}", and contains one or two arguments. In this example, the first argument, a, represents the minimum number of matches required and the second, b, represents the maximum number of matches for the expression to be true. In our example {2,6} is the quantifier.

The other quantifier in this email example if the +. In regular expressions + stands for one or more. In this example + states that there must be one or more matching characters for the bracketted expression to return true.
 
### Character Classes

Character classes are used to specify which characters to match. In our example, the first character class is "[a-z0-9_\.-]". This includes two character ranges, a-z, which will match any lowercase letters between a and z and 0-9 which will match any digit between 0 and 9.

### Grouping and Capturing

Grouping expressions allows us to extract the characters of a group for validation. Text found between paranthesis "()" is defined as a group. In the example the groups are as follows:
"([a-z0-9_.-]+)"
"([\da-z.-]+)"
"([a-z.]{2,6})"

### Bracket Expressions

Bracket expressions show us which characters must be matched. In our example, the bracket expressions are:
"([a-z0-9_\.-]+)" - this group shows that all characters, a-z and all numbered characters  0-9 will be matched.
"([\da-z\.-]+)" - the second looks for a-z characters and checks the character \d for a matching digit.
"([a-z\.]" - finally, this group verifies that characters a-z are matched.

### Greedy and Lazy Match

Greedy matches tell search engines to match as many instances of its qualified token as possible. Think of it like this, greedy matches want as much as possible (hence the name) In contrast lazy matches (the shortest match) tell the search engine to match as few of the quantified tokens as possible. The lazy matches want as little as possible (you may notice a naming pattern).
In the example, the "+" quantifier is a greedy match. It will ensure a search of as many quantified tokens are possible.

## Author

Hello! My name is Jimmy Morgan. I am a student studying to be full stack web developer through The Ohio State University. You can find my Github here:
GitHub: [https://github.com/ek33450505](https://github.com/Jmorg21)
