# Regex-to-Match-an-Email

## What Is a Regex?

Short for regular expression, a regex is a string of text that allows you to create patterns that help match, locate, and manage text.
In JavaScript, regular expressions are also objects. These patterns are used with the exec() and test() methods of RegExp, and with the 
match(), matchAll(), replace(), replaceAll(), search(), and split() methods of String. 

## Summary

You may have gone through even more complex tasks involving text transformation in your day to day life. It may take a lot of time and also produce some errors, 
because we are human, we hate boring things.Learning regex can be known as a lifetime investment.
For example, the following regular expression can be used to verify that user input is a valid email address:
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/.

## Anothe example
![regular-expression](https://user-images.githubusercontent.com/89751266/155612654-1d5e2b98-62ef-4d35-81ba-9e993037fb24.gif)

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
When using regular expressions in a programming language to validate user input, using anchors is very important.
Anchors do not match any character at all. Instead, they match a position before, after, or between characters.
as you can see the exaple above 
^ – The caret anchor matches the beginning of the text.
$ – The dollar anchor matches the end of the text.

### Quantifiers
Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found.

\* *?	Match zero or more times.\
\+ +?	Match one or more times.\
\? ??	Match zero or one time.\
\{ n }	{ n }?	Match exactly n times.\
\{ n ,}	{ n ,}?	Match at least n times.\
\{ n , m }	{ n , m }?	Match from n to m times.\
Quantifiers in this regex includes the + operator, which will connect the users email name + email service + .com. Another quantifier for this regex includes {2,6},
which will allow a match range of 2-6 characters for the character set of [a-z\.].

### OR Operator
The "or" operatorin a regular expression using the | element.
For example, [a-f0-9]{7}|[a-f0-9]{4}
This means that our value could either be 7 characters or 4 characters.
in email validation we did not use OR operation.

### Character Classes
Simply to match only one out of several characters. Simply place the characters you want to match between square brackets.
For example, [A-Za-z_][A-Za-z_0-9].

### Flags
Regular expressions have flags that affect the search.
i =>  case-insensitive: no difference between A and a 
g =>  global , without it – only the first match is returned.
m =>  Makes the boundary characters ^ and $ match the beginning and ending of every single line instead of the beginning and ending of the whole string.
s =>  Enables “dotall” mode, that allows a dot . to match newline character \n
u =>  Enables full Unicode support. The flag enables correct processing of surrogate pairs. 
y =>  Makes the expression start its searching from the index indicated in its lastIndex property.
in email validation we did not use any flags.

### Grouping and Capturing
capturing group  has two effects:
1 - It allows to get a part of the match as a separate item in the result array.
2 - If we put a quantifier after the parentheses, it applies to the parentheses as a whole.
the capturing group 1 in this expression is ([a-z0-9_\.-]+) that matches the user email name. 
The second capturing group is ([\da-z\.-]+) which will match the email service.
Then lastly, capture group #3 is ([a-z\.]{2,6}) to capture the .com.

### Bracket Expressions
Bracked expressios for email validation includes the character sets of [a-z0-9_\.-], which is matching any letter a-z and is case senstive. 
It also matches a character 0-9 and matches the characters "_" , "-" , and "."; [\da-z\.-], 
which is matching a single digit from 0-9, any character a-z (case senstive),
and the characters "." and "-".; [a-z\.] matches any character a-z(case senstive) and the character ".".

### Greedy and Lazy Match
This regrex includes greedy matches. Since it includes the + Quantifier, it will match as many times as possible giving back as needed. 
Another greedy Quantifier used in this regex is {} when matching `{2,6} for the last capture group.
'Greedy' means match longest possible string.
'Lazy' means match shortest possible string.

### Boundaries
A word boundary, in most regex dialects, is a position between \w and \W (non-word char), or at the beginning or end of a string if it begins or ends 
(respectively) with a word character ([0-9A-Za-z_]).

### Back-references
Backreferences match the same text as previously matched by a capturing group.
Back-references and subexpressions are used in two cases: in the regular expression search pattern, and in the replacement part of the s command.

### Look-ahead and Look-behind
Lookarounds are zero width assertions. They check for a regex (towards right or left of the current position - based on ahead or behind), 
succeeds or fails when a match is found (based on if it is positive or negative) and discards the matched portion. 
example 
(?=foo)	Lookahead,	Asserts that what immediately follows the current position in the string is foo
(?<=foo)	Lookbehind,	Asserts that what immediately precedes the current position in the string is foo
(?!foo)	Negative Lookahead,	Asserts that what immediately follows the current position in the string is not foo
(?<!foo)	Negative Lookbehind,	Asserts that what immediately precedes the current position in the string is not foo

## Author
### Abdurraouf Sadi
### Full stack web developer 
[![317725_linkedin_social_icon](https://user-images.githubusercontent.com/89751266/140631331-e97c3a6d-52f7-4d12-b38f-33ca5a2fad7d.png)][1]
[![GitHub-Mark-64px](https://user-images.githubusercontent.com/89751266/140631675-21779441-b105-4714-a99d-1785de17d460.png)][2]
---
[1]: https://www.linkedin.com/in/abdurraouf-sadi/
[2]: https://github.com/asadi80


Made with ❤️ by Abdurraouf Sadi
