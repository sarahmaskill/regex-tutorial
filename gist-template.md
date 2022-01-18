# Matching an Email

Regular Expressions are a Javascript method you use to check if a string contains a certain character or phrase. In this gist I will be reviewing the Matching an Email Regex


## Summary

Regular expressions, or regex for short, are a series of special characters that define a search pattern. Take the following example of a regular expression, which we’ll call “Matching a Email”:

Matching an Email: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

This pattern can be used as a basic email validation. Below I will break down the different components. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)

## Regex Components

The regex is a literal and the pattern must be wrapped in a "/" like the example below. 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

Lets break down each component below. 

### Anchors

The Matching an Email regex uses `^` and `$` anchors. 

The `^` anchor marks the begining of a string that begins with a character. There are two formats for this anchor. 

- An exact string match. A regex is case sensitive, so this anchor would search for exact matches. As an example ^Dog would match "Dog" and "Dog tag", but not "dog" and "dog tag"

- a range of possible matches. This uses a bracketed expressions. 

The `$` anchor is the oposite of the previous anchor. It searches for a string that ends with the characters that precede it. 

### Quantifiers

This regex uses the `+` which connects the email name, email provider, and the top level domain is for the email. 

### Grouping Constructs

This regex has three groups seperated by the quantifier 

- ([a-z0-9_\.-]+)
- ([\da-z\.-]+)
- ([a-z\.]{2,6})

Together these form emailName@emailProvider.topLevelDomain

### Bracket Expressions

This regex holds the bracketed expression character sets of [a-z0-9_\.-], which is matching any letter a-z and is case senstive. It also matches a character 0-9 and matches the characters "_" , "-" , and "."; [\da-z\.-], which is matching a single digit from 0-9, any character a-z (case senstive), and the characters "." and "-".; [a-z\.] matches any character a-z(case senstive) and the character ".".

### Character Classes

This expression uses the character class `\d`. `\d` will match a single digit from 0-9. It also uses `.` to match any character except the newline character.


### Character Escapes

The `\` in this expression escapes the character that would be searched for. In this example `.-` would not be searched for in the regex for the emailName.

## Author

This was written by [@sarahmaskill](https://github.com/sarahmaskill)
