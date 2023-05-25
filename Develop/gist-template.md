# Regex Tutorial

A regex, which is short for regular expression, is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input.

## Summary
In this tutorial, we will be focusing on a regular expression that matches a URL. 

```
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
```

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
<!-- - [Flags](#flags) -->
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components
```
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
```
### Anchors

`^`  `$`

`^` - The caret symbol denotes the start of the string. This means that the pattern must match from the beginning of the string.

`$` - The dollar sign represents the end of the string. It ensures that the pattern must match until the end of the string.

### Quantifiers
`?` - The question mark quantifier makes the preceding element optional. In this expression, it applies to `(https?:\/\/)`, allowing the "s" in "https" to be optional.

`+` - The plus symbol quantifier matches one or more occurrences of the preceding element. It is used with `([\da-z\.-]+)` to match one or more domain/subdomain characters.

`{2,6}` - The curly braces with the range {2,6} specify the minimum and maximum number of occurrences of the preceding element. It is used with 
`([a-z\.]{2,6})` to match TLDs with a length between 2 and 6 characters.

`*` - The asterisk quantifier matches zero or more occurrences of the preceding element. It is used with `([\/\w \.-]*)` to match zero or more path segments.

### OR Operator
`|` - The vertical bar acts as an OR operator. It allows for multiple options to be matched. However, it is not present in the given regular expression.

### Character Classes
`[]` - Square brackets define a character class, which matches any single character within the brackets. In this expression, it is used to define character ranges and sets.

`[\da-z\.-]` - This character class matches a single character that can be a digit `\d`, a lowercase letter `(a-z)`, a dot `.`, or a hyphen `-`.

`[a-z\.]` - This character class matches a single lowercase letter `(a-z)` or a dot `.`. It is used in `([a-z\.]{2,6})` to match TLDs.
<!-- ### Flags -->

### Grouping and Capturing
```
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
```

`()` - Parentheses are used for grouping and capturing in regular expressions.

`(https?:\/\/)?` - This group captures the protocol portion (HTTP or HTTPS) of the URL and makes it optional.

`([\da-z\.-]+)` - This capturing group matches and captures the domain name or subdomain of the URL.

`([a-z\.]{2,6})` - This capturing group matches and captures the top-level domain (TLD) of the URL.

`([\/\w \.-]*)` - This capturing group matches and captures the path segments of the URL.

`([\/\w \.-]*)*` - This grouping with the asterisk quantifier allows for capturing zero or more occurrences of the path segments.

### Bracket Expressions

### Greedy and Lazy Match

<!-- ### Boundaries -->

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
