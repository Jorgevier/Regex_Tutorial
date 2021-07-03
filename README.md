# Regex_Tutorial




## Summary

translating a Regex to match an email

Matching an Email: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

Matching an Email: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/




## Regex Components



### Anchors
For the above, the anchors on this is /^ and $/. The /^ refers to the start of the String. and $/ refers to the end of the string. So ([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6} is our outline to match our email

---
### Quantifiers
Quantifiers sets the limits that the string(email) will have, for example the length is min 2 character and max of 6 characters for the second part of the email. its stated with {}.

---

### Grouping Constructs
The above has 3 grouping constructs above. plus 2 literal sign which means that the email we are search must contain an @ symbol after the first group and must have a . after the 2nd group. please note that the \ before the . just means a . 
When you have () between() they are looking for the litteral character not a range

---

### Bracket Expressions
The [] are Bracket expressions. It hold in the character classes to help breakdown what the email contains. but the hold a range or characters. if it was a literal character that must be in there than it doesnt need a bracket. for example in matching an email the @ and . symbol does not need one because @ and . must be included

---

### Character Classes
Character classes are in brackets. It doesnt show the length of the string but it show everything that may be included in it. its also cap sensitive.

[a-z0-9_\.-] = it may have any lowercase letter from a to z.
               any number from 0 to 9 
               it may include special charater but only _ . -
               length is not meantion, string 
               could contain all of them or just 1, 2 or 3 group.
               fyi - puting a forward slash infront of a period mean just period
                     \.  is equal to just . 

for example- jorge
             j0rge
             jorge_passed
             j0rge-.pass_
             --__..-
             8675309


[\da-z\.-] = \d means any number from 0 thru 9
             it may have any lowercase letter from a to z
             it may have a period(.) or a -
             length is not meantion, string 
             could contain all of them or just 1, 2 or 3 group.

for example- jorge
             j0rge
             jorge-passed
             j0rge-.pass
             --..-
             8675309


[a-z\.]{2,6} = it may have any lowercase letter from a to z
               it may have a period(.)
               length here is minimum 2characters, max 6 characters

for example- jorge
             j0rge
             jv
             ...123
             abc...
             867530

---

### The OR Operator
In my example to match an email i have no OR Operator but its taking to expresions in () and making them equal or true

i am (21|41) years old = "i am 21 years old" or "i am 41 years old" - TRUE!

---

### Flags
Matching an email does not have any of the 6 flags in it

---

### Character Escapes
[\da-z\.-] 
The  \d is an escape it mean any number from 0 thru 9

---

## Resourses
-youtube, 

-google, 

-https://javascript.info/regexp-introduction

---

## Author
by Jorge viera,

any questions please email me at : brolly417@aol.com
