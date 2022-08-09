# How to write a Regular Express to validate and email
When an input of an email is required by a user, you may want to validiate that in fact the user has entered a email address. You can use a regular expression to do this. 
<br>
In this gist I will explain how to write the following regex and explain how it works.

` /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
## Summary
A regular expression can be used let check if the user has entered something that matches an email format.
An email has four parts;
- the 'username' section also known as the local part or recipient name. It can have letters, numbers and special characters.
- after the recipient name comes the @
- the domain name which can use letters, numbers, a . or -
- the top level domain which starts with a . and finishes with between 2 and 6 letters.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)


## Regex Components
### Anchors
the `^` is the begining anchor and the `$` us the end anchor.
 Syntax      | Description | 
|  :----:        |    :----:   |    
 ^[a-z0-9_\.-]+      | start matches with letters a-z, num 0-9, underscore, period, or hyphen|
 ([a-z\.]{2,6})$    |end matches with letters a-z, or a period|  
 ### Quantifiers
 A qualifier shows how many characters can be used in a given section.  It follows the character rule. In this example it is the plus symbol `([char]+)` and the valyes inside the curly brackets`([char]{2,6})`.
 Syntax                       | Description | 
|   :----:                      |    :----:   |    
|  [\da-z\.-]+    | matches one or more specified characters|
| ([a-z\.]{2,6})$      | matches within two to six characters| 

### OR Operator
This is what kinds of characters can be in a section, this is represented by what is inside the square brackets `[char]`. Only characters that match what are represented inside the square brackets can be validated.
|  Syntax                       | Description | 
|   :----:                      |    :----:   |    
| [a-z0-9_\.-]   | matches with any character inside the brackets from a to z,upper and lowercase, any number, or a _ \ .-|  
### Character Classes
Character classes specifies set of characters that need to be matched. This is represented by `\`. Here it is "digits" `\d`.

 Syntax                       | Description | 
  :----:                      |    :----:   |    
 [\da-z\.-]  | matches with digits, letters from a to z, underscore, hyphen or period|  
 
 ### Grouping and Capturing
 Strings that should be matched are grouped together inside `()` In the email regex email there are three groups indicated by the parentheses.
 |  Syntax                       | Description | 
|    :----:                      |    :----:   |    
| ([a-z0-9_\.-]+)@([\da-z\.-]+)      | encloses group of regex to be matched to|

### Bracket Expressions
Inside the paretheses there will be brackets `[]` that indicate what kind of characters need to be matched. There will be a range. In the first ([char]) example it can be a through z lowercase, numbers 0-9, and special characters
|Syntax                       | Description | 
|    :----:                      |    :----:   |    
|  ([a-z0-9_\.-]+)@([\da-z\.-]+)    | encloses set of characters to be matched to|


### Escaped Characters
Escaped characters are to show what the literal value of a special character by adding a backslash `\` in front of the special character.

| Syntax                       | Description | 
|   :----:                      |    :----:   |    
|/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/  | for this example the escaped character is the period|

## Author
This Gist is written by Natalie Fairbourne ♥️
- [GitHub Profile](https://github.com/nadybee)
- natalie@yoodlize.com
