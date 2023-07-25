# Regex codes explained

Regex codes are strings of seemingly random characters that are used to search through text for specific things. They can be used to validate usernames, emails, passwords, or practically anything you can imagine.

## Summary

I will be explaining the functionality of password strength regex codes. These can detect (roughly) how strong your password is based on some pregenerated criteria.
```
/^[a-zA-Z0-9_-]{8,12}$/
/^[a-zA-Z0-9?!_-]{8,12}$/
/^[a-zA-Z0-9?!_-]{12,16}$/
```
Each of the previous regex codes detects a progressively stronger password.

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
The ^ and \$ at the beginning and end of the regex are there to make sure the password is the only thing in the text. The ^ matches the start of the text and the \$ matches the end. Therefore, the password must be the only thing in the text.

### Quantifiers
The {8,12} means that the text its matching to must be at least 8 characters long and less than 12 long. You can see this increase to detect a stronger password in the 3rd regex. 

### Grouping Constructs
'()' are used to group regex. It allows you to handle 2 expressions separately. 

### Bracket Expressions
The bracket expression in the first regex detects any letters, numbers, along with underscores and hyphens. The next 2 regex's detect ?'s and !'s as well.  
  

\[a-zA-Z0-9_-\] can be viewed in 4 groups. a-z detects all lowercase letters. A-Z detects all uppercase. 0-9 detects all numbers. The last _- are used to add underscores and hyphens to the bracket expression.  
  
  This bracket expression will match any string of text that contains these characters.

### The OR Operator
The OR operator, '|', is not used in these codes, but it does exactly what you think it does. The expression A|B would search for text that matches A OR B, assuming A and B are complete expressions.

### Flags
Flags don't have a big use for passwords, as flags are placed after the closing bracket to specify more information. A flag of m means that the regex would search for matches that could possibly span multiple lines.

### Character Escapes
The character escape, '\', can be used to allow the regex to search for things that would normally be used to store information. Trying to put a '\[' inside of a regex would cause it to initiate a bracket expression, but a '\\[' would allow it to search for '\['

## Author

 - Email: kyleslaughter8@gmail.com
 - Github: [KyleSl](https://github.com/KyleSl)
