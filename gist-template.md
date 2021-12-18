# Regex Tutorial

Regex (or regular expression) is a sequence of characters that define a pattern for a specific search. They can be used in code or algorithms in order to find certain patterns of characters in a string. Regular expressions are often used to validate some input.

## Summary

A regular expression to match an email would look like this: 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` 

This regular expression will be described using terms frequently used in regex expressions like Anchors, Quantifiers, Grouping Coonstructs, Bracket Expressions, Character Classes, The OR Operator, Flags, and Character Escapes.

Here is an example of code using JavaScript and a regex expression validating an email:

function ValidateEmail(mail) 
{
 if (/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/.test(myForm.emailAddr.value))
  {
    return (true)
  }
    alert("You have entered an invalid email address!")
    return (false)
};

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
In our email matching regex expression(^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/), anchors can be signified by ^ and $. The ^ anchor signifies a string that begins with the characters that follow it. The $ anchor signifies a string that end with the characters that precede it. 

### Quantifiers
In our email matching regex expression(^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/), anchors can be signified by the characters {2,6} just before the anchor $, and the +. Quantifiers set the limit to a string that the regex matches. The + character matches the whatever expression that precedes it one or more times. In our case, the bracket expression [a-z0-9_\.-] has the quantifier + meaning any characters a-z,0-9, or _\.- has to match at least 1 or more times. The same is true for the other bracket expression in our email match. The other quantier {2,6} sets the limit of characters in the string for the bracket expression [a-z\.] to be between 2-6 characters.
Quantifiers include: 

*—Matches the pattern zero or more times

+—Matches the pattern one or more times

?—Matches the pattern zero or one time

{}—Curly brackets can provide three different ways to set limits for a match:

{ n }—Matches the pattern exactly n number of times

{ n, }—Matches the pattern at least n number of times

{ n, x }—Matches the pattern from a minimum of n number of times to a maximum of x number of times


### Grouping Constructs
Regex is very open-ended an match with as many possibilities as possible. In order to create a more narrow search, grouping contructs help fullful different requirements. They create by using the charcters () and adding other characters within them. In our example, it is broken into three contructs, (/^([a-z0-9_\.-]+)      ([\da-z\.-]+) and ([a-z\.]{2,6}). 


### Bracket Expressions
Anything in between [] is a bracket expression that represents the range of characters that should be matched. For our email example, [a-z\.] means any range of characters a-z or . 

### Character Classes
Character classes can be used to search a range of characters in a regex engine. In our email match example, [a-z0-9_\.-] is a character class that looks at a range of characters from a-z or 0-9 or _ or \ or . or - . Character classes only match single characters. For instance, in a regex expression like gr[ae]y, either gray or grey would match while graay or graey will not. 


### The OR Operator
The OR Operator can be expressed using the | character. This character can be used outside of bracket logic where there is already an or operator. 

### Flags
Flags are placed at the end of a regex, after the second slash, and they define additional functionality or limits for the regex. There are six optional flags that can be used, either separately or together and in any order, but these are the three you're most likely to encounter:

g—Global search: the regex should be tested against all possible matches in a string.

i—Case-insensitive search: case should be ignored while attempting a match in a string

m—Multi-line search: a multi-line input string should be treated as multiple lines

### Character Escapes
The \ character in a regular expression escapes a character that would otherwise be taken litterally. In our example, \. is taken literally between ([\da-z\.-]+) and ([a-z\.]{2,6})$/). This means there should be a literally . between these two grouping constructs.

## Author

I am a Full Stack Developer trying to further my knowledge in the computer programming and tech world. Other hobbies I enjoy are soccer, rowing, and hiking. A link to my Github is: https://github.com/degrootr253 
