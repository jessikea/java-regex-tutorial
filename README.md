# Java Regex Tutorial: Matching an HTML

# Title (replace with your title)
This tutorial delves into how regular expressions can be applied in Java for effective pattern matching and text processing. Specifically, it focuses on crafting a regular expression that can identify an HTML tag within a text string. This skill can prove to be valuable in tasks such as parsing HTML documents or retrieving data from web pages.

## Summary

The regular expression we will be describing is:
/^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/
This regular expression identifies an HTML tag present in a string and captures its name, attributes, and content (if any) in separate groups. Moreover, it enables recognizing self-closing tags that contain no content.
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
The ^ and $ anchors match the beginning and end of the string. This ensures that the entire string matches the pattern.

### Quantifiers
The + and * quantifiers are used to match one or more or zero or more occurrences of the previous character or group, respectively. In this regex, they are used to match one or more lowercase letters (a-z) in the tag name, and attributes that are greater than zero



### OR Operator
The | operator in regular expressions is applied to match either of the two provided alternatives. In the present case, it is employed to recognize either a closing tag that has content or a self-closing tag that contains no content.
### Character Classes
The [a-z] character class matches any lowercase letter from a to z, used to match the tag name.
### Flags

### Grouping and Capturing
The () parentheses are used to capture groups of characters in the regex. 
There are three groups in this case: 
1. The tag name, captured using ([a-z]+)
2. Zero or more attributes, captured using ([^<]+)*
3. The content of the tag (if any), captured using (.*)
### Bracket Expressions
The [^<] bracket expression matches any character that is not a <. 
### Greedy and Lazy Match
The * and + quantifiers are greedy and will match with as many characters as it can. To make them lazy, matching with fewer characters, a ? is added after them. 

### Boundaries
The ^ and $ anchors are used to match the beginning and end of the string as mentioned previously.

### Back-references
To ensure that the closing tag corresponds to the opening tag, the \1 back-reference is utilized, which matches the same text as the first capture group (i.e., the tag name) in the closing tag.
### Look-ahead and Look-behind

## Author

Jess Tran: https://github.com/jessikea