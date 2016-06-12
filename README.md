# JavaScipt ES6 RegExp Cheatsheet


#### 資料來源：[MDN JavaScript RegExp](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)
#### 資料整理：[cashbook](https://github.com/cashbooktw/)
---

### Syntax
/pattern/flags <br>
new Regexp(pattern[,flags])

---

### Special characters meaning

|Boundaries||
|:--|:---|
|^|Start of string
|$|End of string
|\b|A word boundary
|\B|Non-word boundary

||Character classes|
|:---|:---|
|.|Any single character
|\s|Any whitespace character
|\S|Any non-whitespace character
|\d|Any digit
|\D|Any non-digit
|\w|Any word character
|\W|Any non-word character
|\t|Tab
|\r|Carrige return
|\n|NewLine
|\v|Vertical whitespace character
|\f|Form-feed
|[\b]|Backspace character (Not to be confused with \b)
|\0|Null character
|\cX|Control character X (X is a letter from A-Z)
|\xhh|Hex character hh (two hexadecimal digits)
|\uhhhh| Matches the unicode character with the given hex value (four hexadecimal digits)
|\ddd|Octal character ddd
|\|Makes any character literal
|\u{hhhh}|U+hhhh (only when u flag is set)

||Quantifiers|
|:---|:---|
|a?|0 or 1 of a
|a*|0 or more of a
|a+|1 or more of a
|a{3}|Exactly 3 of a
|a{3,}|3 or more of a
|a{3,6}|Between 3 and 6 of a
|a*|Greedy quantifiers
|a*?|Lazy quantifiers

||Grouping and back references|
|:---|:---|
|(...)|Capture everything enclosed
|(?:...)|Match everything enclosed (no capture group)
|\n|Match nth subpattern (n=number)

||Assertions|
|:---|:---|
|(?=...)|Positive lookahead
|(?!...)|Negative lookahead

||Character Sets|
|:---|:---|
|[abc]|A character of: a, b or c
|[^abc]|A character except: a, b or c
|[a-z]|A character in the range: a to z
|[^a-z]|A character not in the range: a to z
|[a-zA-z]|A character in the range: a to z or a-z

||Alternation|
|:---|:---|
|(a&#124;b)|Match either a or b

||Flags/Modifiers|
|:---|:---|
|g|Global
|m|Multiline
|i|Case insensitive
|u|Unicode
|y|Sticky

---

### Properties

||RegExp|
|:---|:---|
|prototype|Allows the addition of properties to all objects.
|lastIndex|The index at which to start the next match.

||RegExp.prototype|
|:---|:---|
|flags|A string that contains the flags of the RegExp object.
|global|Whether to test the regular expression against all possible matches in a string.
|ignoreCase|Whether to ignore case.
|multiline|Whether or not to search in strings across multiple lines.
|source|The text of the pattern.
|sticky|Whether or not the search is sticky.
|unicode|Whether or not Unicode features are enabled.

---

### Methods

||RegExp.prototype|
|:---|:---|
|exec()|Executes a search for a match in its string parameter.
|test()|Tests for a match in its string parameter.
|[Symbol.match]|Performs match to given string and returns match result.
|[Symbol.replace]|Replaces matches in given string with new substring.
|[Symbol.search]|Searches the match in given string and returns the index the pattern found in the string.
|[Symbol.split]|Splits given string into an array by separating the string into substring.
|toString()|Returns a string representing the specified object.
