# JavaScript's Regex

This is an in-depth look at the Regex library that comes packaged with JavaScript. To dive deeper into how regex works, I will be using examples from code snippets found in [this repo](https://github.com/triestpa/You-Should-Learn-Regex.git) by [triestpa](https://github.com/triestpa).  

## Summary

Regular Expressions are used as advanced search patterns within strings. With matching patterns, users are able to find, replace, and remove the queried pattern from whatever body of text they are targeting. For this assignemnt, I will be taking an in-depth look at the regex library that is used with JavaScript. 

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
This regex contains two methods, exec() and test(). These methods are often used in combination with the string methods that JavaScript posesses. For the purposes of this tutorial, triestpa mainly uses the exec() method to seach strings.

### Anchors
Regex Anchors are used to notate positions, rather than characters. There are to anchor characters in JavaScript's Regex function. 
- ^ - which is used to mark the beginnig of the string.
- $ - which is used to mark the end of the string.

### Quantifiers
Quantifiers determine the number of instances a string must have for the searched pattern. 
- \+ - means there must be at least one occurence of the pattern in the string.
- \* - means there can be 0 or more of the preceding character (continues for each matching character).
- ? - means there can be 0 or more of the preceeding character (stops after first instance).
- {X} - specifies the number of characters that must be in a row. 
- {X, Y} - matches a sequence of numbers from x to y. 
- {X,} - matches any squence of X numbers. 
- ?= - matches any string that is followed by whatever character is placed after the =. 
- ?! - matches any string htat is NOT followed by whatever character is placed after the =. 

### OR Operator
A single | is used to as an OR operator in the JavaScript regex. If multiple patterns are being searched, they can each be seperated with the |. 

### Character Classes
Character classes determine the type of character being searched for.
- [abc] or [a-c] - These patterns do the same thing. The first matches each of the characters listed, while the second matches any characters within the range specified. 
- ^ - Using this NOT operator in front of the patterns (within the brackets), means it matches any strings that do NOT contain the specified characters (or characters within the range).
- . - Can match the literal . or can denote that a character must have something either before or after it. 
- d - Matches any numeric value. 
- D - Acts as the NOT operator for d. 
- w - Matches any character (excluding special characters).
- W - Acts as the NOT operator for w.
- s - Matches spacing.
- S - Acts as the NOT operator for s.

### Flags
Flags are a way to specify some of the allowed parameters within a search. 
- i - specifies case does not matter for the characters used in the pattern.
- g - returns all instances of the pattern, instead of just the first.
- m - traverses multiple lines of a queried string.
- s - allows a dot to act as a newline character.
- u - allows Unicode support.
- y - searches the exact position of the pattern.

### Grouping and Capturing
In Javascript's regex, [] denote groups of characters that are being searched for, as mentioned above. () means either of the patternes (separated by the | operator) can appear in the queried text. 

### Bracket Expressions
Bracket expressions simply reference the form-factor of the grouping characters. 

### Greedy and Lazy Match
Greedy and lazy determine what is returned from a matching pattern. For instance, the difference between the * and ? quantifiers. * is considered greedy, because it will continue for each sequential matching character, where as ? will stop after the first instance. 

### Boundaries
The boundary operator \b is used to search word positioning. For instance, if you were to look for a word \bram\b, and you had the scentence, "Dodge has a truck line called ram." it will match the word ram at the end of that scentence. However, if you had the scentence, "I am a programmer." the word ram within programmer would not be returned, because it does not stand on its own. 

### Back-references
Back references are used to store a found value (can be done based on symbol \1 or name \k), and group items found in between those symbols/named instances. 

### Look-ahead and Look-behind
There is a combination of four types of "lookaround" operators:
- X(?=Y) - This pattern is called a positive lookahead, and would match any instance of X that is followed by Y.
- X(?!Y) - Is the negation of the previous example. Known as a negative lookahead.
- (?<=Y)X - This pattern is called a positive lookbehind, and would match any instance of X that is behind Y. 
- (?<!Y)X - Is the negation of the previous example. Known as a negative lookbehind. 

### Examples
In the repo referenced above, triestpa gives a few examples we will take a look at. The first being:

```
  const regex = /\b(0?[1-9]|[12]\d|3[01])([ \/\-])(0?[1-9]|1[012])\2(\d{4})/
  const str = `Today's date is 18/09/2017`
  const subst = `$3$2$1$2$4`
  const result = str.replace(regex, subst)
  console.log(result)
```

In this example, 


## Author
[Theo Greer](https://github.com/tdgreer1203)

I am an aspiring software developer who is currently learning JavaScript. My interests are in fullstack development, and I would like to work for a company with a great training/mentoring program. I feel this would be critical to my success in the industry. I currently reside in the Orlando area, and am open to any/all local/remote positions. 
