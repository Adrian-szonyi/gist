# Regex Tutorial

## Description

For this tutorial I will be explaining how the following regular expression works:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

This regex is used to find any email addresses in a text file. This tutorial will breakdown how each individual element works. The class groupings are separated by the `@` and `.` symbols as is the standard format for all email addresses. This is a really handy regex to use to locate all email addresses in a large text file which can help with privacy protection as you might want to black out or remove the addresses.

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

The regular expression chosen has two anchors which are as follows: `^` and `$` 
First off the `^` anchor is used to indicate that this regex is searching for a term that is at the start of a new line.
Secondly the `$` anchor is used to search for a term that is at the end of a line. 

Together this means that the regex will match any emails that are at either the start or end of a line.

### Quantifiers

There are a few different quantifiers being used in this regex. The first example is the `+` used at the end of the first grouping construct. This quantifier means that the result has to have 1 or more of the potential elements outlined in that grouping construct.
The `+` quantifier is used in the second grouping construct as well. Both of them are looking for a term with 1 or more elements that meet the construct criteria.
Finally in the third grouping contstruct the `{2,6}` quantifier is used to signify that this grouping construct requires a character length between 2 and 6.

### Grouping Constructs

There are three separate capturing groups or grouping constructs in this regex example. 
The first one is `([a-z0-9_\.-]+)`
This grouping is looking for 1 or more characters that are either any letter, any number, could include a `_`, a `-` or a `.`
The `\.` part is used to break up the special characters so that it doesn't also look for a term that includes `_.-` as one string. The regex is looking for any emails that contain either a period, underscore or hyphen in the start of the email address.

The next grouping construct is: `([\da-z\.-]+)`
This one is looking for any number and/or any letter or a `.` or a `-`. At least one character is required that meets the criteria. This the part of the email after the @ symbol.

The final grouping construct is: `([a-z\.]{2,6})`
This represents the part of the email address after the `.` used for the email domain. 
The grouping is looking for anywhere between 2 or 6 characters that could be either a letter or a `.`
This means that the domain part of an email address can't include a number and has to have at least 2 letters and a max of 6.

### Bracket Expressions

The bracket expressions are as follows:

`[a-z0-9_\.-]` This first expression is looking for any letter or number or a period, hyphen or underscore.
`[\da-z\.-]` This one is looking for any number or letter a period or a hyphen.
`[a-z\.]` Finally this one is looking for any letter or a period.

### Flags

There are no flags being used for the regex example for this tutorial. But the global search and multi-line flags would be recommended when using this regex. They are g and m respectively.

### Character Escapes

The escaped character in this regex example is the period denoted by `\.` in the class groupings. This is used to break up the special characters in the bracket expression so that the regex knows to return any results that also contain a period.

### Author

I am learning to become a full stack developer and have almost finished a 6 month part time course. Feel free to check out my Github link below:
My Github Profile link: [_here_](https://github.com/Adrian-szonyi)
if you have any additional questions you can reach me using the details below:

Email: aszonyi49@gmail.com
