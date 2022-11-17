# Lexical Structure
The lexical structure of a programming language is the set of elementary rules that specifies how you write programs in that language.\
It covers:
* Case sensitivity, spaces, and line breaks
* Comments
* Literals
* Identifiers and reserved words
* Unicode
* Optional semicolons
Javascript is case sensitive.

## Comments
```javascript
// This is a single-line comment.
/* This is also a comment */ // and here is another comment.
/*
 * This is a multi-line comment. The extra * characters at the start of
 * each line are not a required part of the syntax; they just look cool!
 */
```
## Literals
A literal is a data value that appears directly in a program. The following are all
literals:
```javascript
12 // The number twelve
1.2 // The number one point two
"hello world" // A string of text
'Hi' // Another string
true // A Boolean value
false // The other Boolean value
null // Absence of an object
```

## Identifers and Reserved Words
An identifier is simply a name. In JavaScript, identifiers are used to name constants,
variables, properties, functions, and classes and to provide labels for certain loops in
JavaScript code. A JavaScript identifier must begin with a letter, an underscore (_), or
a dollar sign ($). Subsequent characters can be letters, digits, underscores, or dollar
signs. (Digits are not allowed as the first character so that JavaScript can easily distinguish identifiers from numbers.)

These are all legal identifiers:

```javascript
i
my_variable_name
v13
_dummy
$str
```
##  Reserved Words
* let can be used as a variable name
if declared with var outside of a class, for example, but not if declared inside a class or
with const.

* _JavaScript Reaserved Words List:_
  
| 1.    | 2.       | 3.       | 4.         | 5.     | 6.     | 7.    |
| ----- | -------- | -------- | ---------- | ------ | ------ | ----- |
| as    | const    | export   | get        | null   | target | void  |
| async | continue | extends  | if         | of     | this   | while |
| await | debugger | false    | import     | return | throw  | with  |
| break | default  | finally  | in         | set    | true   | yield |
| case  | delete   | for      | instanceof | static | try    |
| catch | do       | from     | let        | super  | typeof |
| class | else     | function | new        | switch | var    |

* JavaScript also reserves or restricts the use of certain keywords that are not currently used by the language but that might be used in future versions:

| 1.         |
| ---------- |
| enum       |
| implements |
| interface  |
| package    |
| private    |
| protected  |
| public     |

## Unicode
* JavaScript programs are written using the Unicode character set, and you can use any
Unicode characters in strings and comments. 
* This means that programmers can use mathematical symbols and words from non-English languages as constants and variables:
  
```javascript
const π = 3.14;
const sí = true;
```
## Unicode Escape Sequences

* Some computer hardware and software cannot display, input, or correctly process the
full set of Unicode characters. 
* To support programmers and systems using older technology, JavaScript defines escape sequences that allow us to write Unicode characters using only ASCII characters.
* These Unicode escapes begin with the characters \u and are either followed by exactly four hexadecimal digits (using uppercase or lowercase letters A–F) or by one to six hexadecimal digits enclosed within curly braces.
* The Unicode escape for the character __“é,”__ for example, is __\u00E9__; here are three different ways to write a variable name that includes this character:

```javascript
let café = 1; // Define a variable using a Unicode character
caf\u00e9 // => 1; access the variable using an escape sequence
caf\u{E9} // => 1; another form of the same escape sequence
```
* Early versions of JavaScript only supported the four-digit escape sequence. 
* The version with curly braces was introduced in ES6 to better support Unicode codepoints that require more than 16 bits, such as emoji:
```javascript
console.log("\u{1F600}"); // Prints a smiley face emoji
```