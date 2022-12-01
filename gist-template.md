# Matching with hex regex
With this walk through we will be looking at how one would go about matching hex values and the ways it can be used. The main uses of hex would be either in RGB color coding mainly used in CSS or with base-10 and base-16 syntax

## Summary
In this walk through we will be using the following regex code snippet:  
`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

In the above code snippet follows multiple small rules that allow us to find any hex code with 6 or three characters
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
To declare the start of a regex you will use the carrot or `^` before you start to create your regex. To declare the ending of a regex you would then enter a dollar sign or `$` this will end youre regex. A simple exampale to see this would look like `/^\d\d:\d\d$/` this is showing that your regex will have two digits followed by a colon and two more digits.
### Quantifiers
There are four different quantifiers `+, *, ? and {n}`. We will only need to use the `?, and {n}` quantifiers they will be explaned further below.

Quantity: `{n}` as being one of the simplest this will help us specifie multiple characters we need `\d{5}` is the same as `\d\d\d\d\d` by adding a `\b` this will exclude any lonfer numbers. We can also do a range this will select the how many characters are needed and how many is to many for example `{3,5}` will select the sequence of characters that is 3 charcters long but no longer then 5. To let the range extend to more characters you will simply use the a snippet `{1,}` this will find the designated charcter starting will a single character and will accept as many that are grouped together.

`?`: this will identify as a 1 or a zero in other words making a symbol optional.
the following pattern `\w+ou?r` will match with both "favor" and "favour".
### OR Operator
The OR operator sounds almost simple as it is with the syntax being `|` you will add this to your regex and it will match with one set or another the following examples will help. 
` let regexp = /html|php|css|java(script)?/gi;
let str = "First HTML appeared, then CSS, then JavaScript";
alert( str.match(regexp) ); // 'HTML', 'CSS', 'JavaScript' `

If you look at the regex code we have you will see that we asking the regex code to match with `/^#?([a-f0-9]{6}` or `|` `[a-f0-9]{3})$/` this will take in two different types of matches.
### Character Classes
There are 3 main types of character classes `\d, \s, \w` which stand for `\d`: digit, a character from 0 to 9. `\s`: space, will repesent the space between, this while also have many other types of spaces that can be added in see [here](https://javascript.info/regexp-character-classes). `\w`: word, this will stand for a "wordly" charcter mainly used for alphabetical characters.

Looking at a small piece of the regex code we can see a simple way to make a match looking at `[a-f0-9]` we can use `/\w-\w\d-\d/`.
### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
