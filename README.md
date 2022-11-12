Regex-Tutorial
Objective
create a tutorial that explains how a specific regular expression, or regex, functions by breaking down each part of the expression and describing what it does

Matching an Email: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
Acceptance Criteria
GIVEN a regex tutorial WHEN I open the tutorial THEN I see a descriptive title and introductory paragraph explaining the purpose of the tutorial, a summary describing the regex featured in the tutorial, a table of contents linking to different sections that break down each component of the regex and explain what it does, and a section about the author with a link to the author’s GitHub profile WHEN I click on the links in the table of contents THEN I am taken to the corresponding sections of the tutorial WHEN I read through each section of the tutorial THEN I find a detailed explanation of what a specific component of the regex does WHEN I reach the end of the tutorial THEN I find a section about the author and a link to the author’s GitHub profile

What Is a Regex?
Regular expression -> regex Regex is a sequence of character that defines a specific search pattern When it's included in code or search algorithms, regex can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are frequently used to validate input.

Example: /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/
lowercase letter between a-z
number between 0-9
string can contain _ or -
string is between 3-16
string must start and end with something that matches the pattern [a-z0-9_-]
Bracket expressions (positive character group):
anything inside the [] represents a range of characters that we want to match ^ can be put in front of a string inside [] to exclude certain characters (negative character)

Qualifiers
set the limits of the string that your regex matches. typically they include the min and max of characters that your regex is looking for. they match as many occurrences of particular patterns as possible.

matches the pattern 0 or more times
matches the pattern 1 or more times ? - matches the pattern 0 or 1 {} - can provide 3 different ways to set limits for a match:
{ n } - matches the pattern exactly n number of times
{ n, } - matches the pattern at least n number of times
{ n, x } - matches the pattern from a min of n number of times to a max of x number of times
example: {3,16} = string has to be between 3-16 characters

Grouping Constructs: to check multiple parts of a string to determine that different sections fulfill different requirements. breaking up sections = (). each section within () is SUBEXPRESSION.

example: (abc):(xyz) subexpression is looking for an exact match

2 Categories:

Capturing - capture the matched character sequences for possible re-use
Non-capturing
A grouping construct can be made non-capturing by adding ?: at the beginning of an expression inside the ()

The OR Operator: by adding | to the grouping contructs, you give it the same logic as bracket expression.

Example: (a|b|c):(x|y|z)

Character Escapes: { used to begin a quantifier { this means that the regex should look for the open curly brace character instead of beginning to define a quantifier.

Character classes: defines a set of characters, any one of which can occur in an input string to fulfill a match.

Flags: regex must be wrapped in slash characters, one exception to this rule is Flags, flags are placed at the end of a regex.