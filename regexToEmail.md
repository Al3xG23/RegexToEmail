# Regex To Email

In this gist tutorial I will be describing the functionality of a particular regex. Regex refers to a regular expression which is used to search a text body through a sequence of characters. The regex will look for particular characteristics as defined within the particular sequence of characters chosen.

## Summary

I will be describing the following regex that should search for emails with a certain pattern. The pattern tells us that the part of the email before the ( @ ) symbol can inlcude one or more instances of lowercase letters from a through z, numbers from 0 through 9, the underscore symbol, the backslash symbol, periods and dashes. After the ( @ ) symbol we can have a section with one or more instances of any Arabic numbers, lower case letters from a through z again, the backslah symbol, periods, and dashes. Then we have an escape character ( \ ) followed by a period that lets us know that the period should be read literally. Finally we have the last part searching for any lowercase letters from a through z, the backslah symbol, periods, and this section can only be between 2 and 6 characters long.

* Matching an Email: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)

## Regex Components

### Anchors

The anchors in a regex define the beginning and end points of the search pattern. For the example I am using The ( ^ ) and the ( $ ) symbols are the anchors. 

The ( ^ ) lets us know that the string must start with the characters that follow it: ( a-z ), ( 0-9 ), ( _ ), ( \ ), ( . ), and ( - ) in the first set of square brackets ( [ ] ).
This would match: "ayn987_\.-0".

The ( $ ) lets us know that the string must end with the preceding characters: ( a-z ), ( \ ), ( . ) and can only be between 2-6 characters long.
This would match: "abiu\.".

### Quantifiers

The quantifiers set the limits of the string or a section of the string. In this instance the ( + ) after the first and second set of square brackets means that everything within the square brackets can be matched one or more times. The curly brackets ( { } ) contain the limits of the length of the string defined by the brackets preceding it. The first number tells us that it should be 2 or more characters long and the second numbers means that it can't be longer than 6 characters long.

### Character Classes

A character class defines a set of characters and in the example ( \d ) represents any Arabic numeral digit. This symbol is actually equivalent to [ 0-9 ].

### Grouping and Capturing

The chraracters wrapped in parentheses define subexpressions. In this example there are three subexpressions: ( [ a-z 0-9 _ \ . - ] ) , ( [ \d a-z \ . - ] ) , and ( [ a-z \ . ] { 2,6 } )

### Bracket Expressions

The ( [ ] ) contain the range of characters we want to match for each part of the string. 

### Greedy and Lazy Match

Quantifiers are greedy by nature, meaning they will always try to match as many times as possibly defined by the character sets you use. We defined the ones used here in the quantifiers section. This example does not include any lazy quantifiers but if we had them they would include the ( ? ) symbol right after the ( + ) symbol meaning match as few times as possible.

### Boundaries

The boundaries are defined by the ( ^ ) and ( $ ) symbols as described in the anchors section.

## Author

My name is Mariel B. and I have been taking a bootcamp course to learn coding. I hope this little tutorial on regex made sense and thank you for your time. Here is a link to my Github profile: https://github.com/Al3xG23.

This is where you can find my gist RegexToEmail.md