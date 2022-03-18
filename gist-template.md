# Regex 

Regex is a formal language theory, is a string that represents a regular language. It is basically a visual expression of testing the strings, when a particular strings matches a expression they turn blue to verify where as different groups with in the expression has its own importantce which explains each piece of expression within the string.

We will be matching a Email and wil go in detail to explain how the Regex expression is defined.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
## Summary

Video Link
https://drive.google.com/file/d/1K-S-r96n_ARXMh7M48y4xUdV9TS_OUG6/view

The expressiong that we have chosen to get into detail is matching the email which can be very useful in terms of authentication where we use the username and password for protecting our account or making it password and username protected. Thats when the regular expressions comes in play and is very beneficial. Lets get into it and will try to decode the expression.

Where the ^ carat sign indicates the start of the string of the overall expression or we can say its the beginning of the string.

Going forward with the expression we have parentheses ( which mainly meaans its captures everything that comes under them like a group. Then we have square brackets [ which means the characters set which matches the characters defined under this set which includes a-z followed by 0-9 which depicts anything between characters a to z and digits between 0 - 9 will match the string. After this we have _ which means the string allows you to enter _ which is accepted and will pass true if entered following the backslah \ with . and - will pass the test if entered within the group. Immediately after that we the square bracket ] to end the character set followed by a plus sign + which depicts to add the token as many times as possible followed by ) closing bracket parentheses to end the group. 

We have a @ symbol to initiates that while checking the email address we need to have the @ symbol after a certain group which mainly coms after entering one or 2 groups as depicted. Then after we have 2nd group to start with the parentheses ( followed by square bracket [ which means to include the character set in accordance with the \d mainly depicts the metacharacter which matches the digits 0 to 9. Then we have a-z which can be included to pass the string by taking any characters between a to z. Following with that we have \. - which mainly means if included within the group will test and pass true followed by square bracket to end the character set. + symbol to to add match the token atleast one time within followed by ) parentheses to end the group.

Here after the second group we have backslash \. which mainly means anything after the second group the . will pass the string to be true and followed by parentheses ( and square bracket [ where any characters between a-z will pass followed by \. by closing the character set.Then we have a quantifier which says {2,6} to match the token atleast 2 times and no more than 6 times followed by the closing bracket to end the parentheses with a $ sign means the end of the line.

So how to tell if the string is true is by checking on regexr.com by passing single groups to check if the expression passes. By breaking down the groups and testing each of them slowly will help to understand the importance of each of them depicted and put across within each character set. Thie site helps to understand the regular expression in more depth with the help of testing online.
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

Regular expression contains multiple components to complete the task when required while Matching Fixed strings, Matching Special Characters, Matching the Characters Sets, Specifying Groups and Fields which means while matching a fixed string defined in the expression, where Matching the special characters is defined as the special characters \|2 matches |2 in the string where the verticle bar in regular expression specifies the alternation and here it matches itself because it follows a backslash. Also with Matching the characters Set it is used where [abc] is to match the letters a,b,c. and also with [^\|] matches any single character excepts the verticle bar where the carat is used to negate the character set.
### Anchors

Anchors are a way of telling you where you at within the expression for say ^ and a $ sign where the ^ means the start of the string and the $ means end of the string. Anchors are mainly same with different languages wheres for some languages it is different and specified within the documentation depending on the use of the language. Also the linke break characters are included within anchors where it handles the line breaks that consist of a single character the same way the dot in the regex. 

### Quantifiers

Quantifiers are mainly describe as +,*,?,{X},$,^,?=,?! whereas they are been termed as greedy as well as lazy and sometimes dont behave as they are have been expected. It mainly tells to either a match the string or match any string that contain certain things. They are also said to be very possesive depenging on how they are being placed within the string. As greedy mainly means that it tells the engine to match as many as tokens of its quantified value or any pattern as possible for example say + will match more than one token \d+ can match more than one digits. Being lazy it means being reluctant where it tell the engine to match few token as needed where ? comes in play where * tells the match more than one characters ? tells to match characters as needed.

### OR Operator

Alternation and grouping are the very much important criteria for a regular expression where if you want to separate different strings you need to use the logical OR operator which is defined by pipe character | For example say "I like to study (CSS|Javascript) but not (Java|Python). These mainly qualifies for more than one string to be true and thats where the OR Operator comes in handy and helps to make more than one string to be true.
### Character Classes

Mainly known as Character Classes or Characters Set it tells the regex expression to match only one out of several characters. It mainly matches the whatever defined between the square brackets []. For example say gr[ae]y where this can match with gray or grey. Also beside this it can contain the numbers within the square bracket too. Moreover with the character set you can use more than one range and match the string for example [a-z0-9A-Z]. There is negated character classes as well where by putting the carat by the opening of the square bracket will negate the character class and as a result will define the character which is not in the character class.
### Flags

Flags in  Javascript is define a its behavior of Searching and are denoted by i, g, s,m, y, u. 
i = It is mainly Ignore Casing and defined as case-insenstive
g = This is mainly the global flag and is used for searching all ocurrences.
s = This flags helps to match new lines and is separated by Dot all .
m = This is multiline flag and is depicted by the starting and ending of each line rather then the string and is specified by boundary characters ^ and $.
y = Sticky flag looks for its particular position or is a lastIndes property.
u = unicode flag is the that matches the 32-bit characters within the regular expression.
https://www.codeguage.com/courses/regexp/flags
### Grouping and Capturing

Grouping and Capturing go hand in hand and mainly means when we define a group wwith in the regex it will capture the text matched by the regex inside them where there is number or a character it will group them accordingly. (gabe){3} then will have gabe 3 times. When using the excape parentheses group they can capture the regex insided them  and also numbers can be reused with a numbered backreference.
https://www.regular-expressions.info/refcapture.html
### Bracket Expressions

Brackets expressions are mainly defined by square bracekts, curly brackets, parentheses and is mainly what a user can see to be looked at whatever is called in between those brackets to match the characters. Where the square bracket [] is defined to match any individual character defined between the brackets. curly brackets {} are generally define to match the exact string and are mainly used after a expression. Parentheses () are mainly the remembered matches and is use to find and replace the operations anytime, and are also used in regex to group different part of the expression into sub-groups as we saw in the email expression.
https://javascript.plainenglish.io/regular-expressions-brackets-f2d6f69ffe13

### Greedy and Lazy Match

As explained earlier above the Greedy by the names means is greedy to take the longest possible string to match and the Lazy by the term speciies will have the approach to take the shortest string possible to match. https://stackoverflow.com/questions/2301285/what-do-lazy-and-greedy-mean-in-the-context-of-regular-expressions

### Boundaries

Boundaries are defined by \b and is generally a anchor same like carat and dollar sign. It is use to define the word character and allows you to perform the search using regular expression in form of \bVeedit\b. Also being said as digits are considered to be the word characters it also helps to set boundaries wherever a digit is implemented. \b7\b this is the same as passing the boundary to the word at the start and at the end of the word. \b matches at any position with in the word as well as between the non-word characters too.
https://www.regular-expressions.info/wordboundaries.html
### Back-references

Backreferences is mainly refered to refer what is already happened previously as a part of regular expression is defined as \ followed by a digit which means if you have one group of character set at the start of the string the back reference will reference the first capturing group the exact same way it was matched. Also if there is / before the backreference it is known as a literal which is nothing but simply the closing of the tag what we are trying to match.
### Look-ahead and Look-behind

They are also defined as Look around and are sometime confusing as what i have looked over the different websites. Look ahead is mainly whatever falls immediately after the current position in the string whereas the Look behind is whatever precides from the current position in the string.
### References

https://cs.lmu.edu/~ray/notes/regex/
https://regexr.com/https://www.rexegg.com/regex-quantifiers.html
https://www.w3schools.com/jsref/jsref_obj_regexp.asp
https://www.regular-expressions.info/anchors.html
https://zone.ni.com/reference/en-XX/help/371714F-01/nirghelp/regular_expressions_components/#:~:text=Regular%20expressions%20can%20contain%20multiple,Specifying%20Groups%20and%20Fields
## Author

https://gist.github.com/veeditparikh2211
https://github.com/veeditparikh2211/RegularExpression
https://gist.github.com/veeditparikh2211/7cc1689f7b474526755b4496085bd458
