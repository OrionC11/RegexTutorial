# A Guide to Regex

This is a tutorial to all things regex, click through the table of contents to reach different sections of the code.

## Summary

Regular expression, or **Regex** for short as it will be referred to for the rest of this tutorial; is a useful method of checking strings to ensure they contain certain letters, numbers or phrases.

An example of how regex looks:
**Matching a Username**-- **/^[a-z0-9_-]{4,12}$/**

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

A regex is considered a literal, what that means is the pattern must be wrapped in forward slashes **/**, and contains many different compononents. Those components include: anchors, quantifiers, grouping constructs, bracket expressions, character classes, the OR operator, flags, and character escapes. Below we'll get into more of what each of those mean.

### Anchors

The Anchor characters are defined as **^** and **$**.

The **^** anchor signifies a string that begins with the characters immediately following it in one of two formats:
    * Exact string matching such as **^Bob** would match strings with "Bob" or "Bob likes pie", but "bob" and "bob likes pie" do not.
    * A range of possible options displayed using bracket expressions which we'll go over further down the line.

The **$** anchor is used to signify a string the Ends with the characters that immediately preceed it, this can be in either format which applies to the **^** operator.

### Quantifiers

Quantifiers are one of the two requirements of regex and determines the number of characters a regex object can be, they can and frequently include both a minimum and maximum number of characters the object can be. Quantifiers are displayed in just before the **$** anchor for example **{4,12}$** would be equivalent to giving a minimum characters of 4 and a maximum characters of 12.

Quantifiers are greedy meaning they match as many occurances of the pattern as possible. Quantifiers include the following operators:
    * *-- Matches zero or more times
    * **+**-- Matches the patern one or more times
    * **?**-- Matches zero or one time
    * **{}**-- Curly brackets provide three different ways to limit a match:
        * **{ n }**-- Matches exactly the number of times specified by **n**
        * **{ n, }**-- Matches at least the number of times specified by **n**
        * **{ n, x }**-- Matches the pattern from a minimum number of times specified by **n** and a maximium number of times specified by **x**

Any quantifier is able to be made **lazy** through the method of adding the **?** operator after it, a lazy quantifier will match as few occurances as possible to it.


### Grouping Constructs

### Bracket Expressions

Bracket expressions are represented through square brackets **[]** and anything which are wrapped within these square brackets represents a range of characters that we want to match.  Another name for these expressions is a **positive character group** because they outline the characters we want to include. We can write these expressions to include any characters we would like to match. In example, **[xyz]** would look for a string which includes the characters **x**, **y**, or **z** regardless of length.

Most often you will see it represented with a hyphen between the letters and numbers of a regex statement **[a-z0-9_-]** would indicate that the range of characters between **a** to **z** and **0** to **9** would all be included. To use the above example this means that writing **[xyz]** would function the same as writing **[x-z]**.

Lets break down the regex statement **[a-z0-9_-]** a little more:
    * **[a-z]**-- This indicates the string can only contain lower case letters between a and z and this only includes letters which are **Lowercase**
    * **[0-9]** -- This indicates all numbers between **0** and **9** are included
    * **[_-]** -- This indicates that the string is allowed to contain underscores **_** and hyphens **-**, both of these are known as special characters.  Special characters include anything which is nonalphanumerical such as punctuations and symbols.


### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
