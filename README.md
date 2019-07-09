# Strings Lab 1

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit

## Question 1
for question1 in 1...10 {
print(String("\(question1)"))
}

print (separator: "")


***
## Question 2

let question2 = 5...51
for evens in question2 where (evens % 2 == 0)
{
print(String(evens))
}


print (separator: "")


***
## Question 3

let question3 = 1...60
for endsFour in question3 where endsFour % 10 == 4
{
print(String(endsFour))
}

***
## Question 4

let question4 = "Hello world!"

for char in question4 {
print("\(char)")
}



print (separator: "")

***
## Question 5


`let myStringSeven = "Hello world!"`

var myStringSeven = "Hello World!"
print(myStringSeven.popLast()!)


var myStringSeven = "Hello World!"
let question5 = String(myStringSeven.last!)
print(question5)


***
## Question 6

Write code that switches on a string, given the following conditions:
- If the string's length is even, print out every character.
- If the string's length is odd, print out every other character.


let question6 = "Why does everyone use, Hello World?"
let numChar: Int = question6.count

if numChar % 2 == 0 {
print (question6)
}
else {
for (num,letter) in (question6.enumerated()) {
if num % 2 != 0 {
print(letter, terminator: "")
}
}
}
print (separator: "")

***
## Question 7

Initialize a String with a character. Show that it is a Character, and not another String, that you're using to initialize it.

let question7: Character = "A"
if question7 == Character("A") {
print("its a character")
} else {
print("its not a character")
}

***
## Question 8 (only did 1)

Build five pairs of **canonically equivalent** strings, the first of each being a pre-composed character and the second being one that uses combinable unicode scalars. Show that they are equivalent.

let accent = "\u{0308}"
let e = "\u{0045}"
let whole = "\u{00CB}"
let actualE = "e"

print(whole.unicodeScalars.sorted())
print(whole)
print(e+accent==whole)
print(e==actualE)


***
## Question 9

**Using only Unicode**, print out `"HELLO WORLD!"`

let helloWorld = "\u{0048}\u{0045}\u{004C}\u{004C}\u{004F}\u{0020}\u{0057}\u{004F}\u{0052}\u{004C}\u{0044}\u{0021}"
print(helloWorld)



***
## Question 10

**Using only Unicode**, print out your name.

let ian = "\u{0049}\u{0061}\u{006E}"
print(ian)


***
## Question 11

**Using only Unicode**, print out `"HELLO WORLD!"` in another language.

let helloWorldSpanish = "\u{0048}\u{004f}\u{004C}\u{0041}\u{0020}\u{004d}\u{0055}\u{004E}\u{0044}\u{004F}"
print(helloWorldSpanish)





***
## Question 12

Print the below flower box using the following information.

- The unicode number for ⚘ is U-2698
- The top and bottom of the box are represented by dashes and the rows are |
- Use the terminator argument in your print statements to print on the same line.
- Hint: It may be useful to try printing out a box of just one character to start then work your way from there.

```swift
Flower Box:
- - - - - - - - - - -
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
- - - - - - - - - - -
```

var flower = "\u{2698}"
var vertical = "\u{007c}"
var horizontal = "\u{005f}"
for _ in 1...11 {
print(horizontal, terminator: " ")
}
print()
for _ in 1...7 {
print("\(vertical) \(flower) \(vertical) \(flower) \(vertical) \(flower) \(vertical) \(flower) \(vertical) \(flower) \(vertical)")
}
for _ in 1...11 {
//    print(horizontal, terminator: " ")
}


***
## Question 13

Write a program that sets up a chess board using Unicode.

```swift
Chess Board:
♖ ♘ ♗ ♕ ♔ ♗ ♘ ♖
♙ ♙ ♙ ♙ ♙ ♙ ♙ ♙




♟ ♟ ♟ ♟ ♟ ♟ ♟ ♟
♜ ♞ ♝ ♛ ♚ ♝ ♞ ♜
```
let whitePieces = "\u{2656}\u{2657}\u{2658}\u{2655}\u{2654}\u{2658}\u{2657}\u{2656}"
print(whitePieces)

let whitepawns = ("\u{2659}")
for _ in 1...8 {
print(whitepawns, terminator: "")
}
let spaces = " "
for _ in 1...4 {
print(spaces)
}


let blackpawns = ("\u{265F}")
for _ in 1...8 {
print(blackpawns, terminator: "")
}

let blackPieces = """

\u{265C}\u{265D}\u{265E}\u{265E}\u{265A}\u{265B}\u{265D}\u{265C}
"""
print(blackPieces)



***
## Question 14

You are given a string stored in the variable `aString`. Create new string named `replacedString` that contains the characters of the original string with all the occurrences of the character `"e"` replaced by `"\*"`.

```swift
var aString = "Replace the letter e with \*"
// 
var aString = "Replace the letter e with *"
let replaced = String(aString.map {
$0 == "e" ? "*" : $0
})
print(replaced)

 ```

Example:

Input:
`var aString = "Replace the letter e with *"`

Expected values:
`replacedString = "R*plac* th* l*tt*r * with *"`

***
## Question 15

You are given a string stored in variable `aString`. Create a new string called `reverse` that contains the original string in reverse order. Print the reversed string.

```swift
var aString = "this string has 29 characters"
var reverse = ""

var aString = "this string has 29 characters"
let reversed = String(aString.reversed())
print(reversed)
```

Example:
Input:
`var aString = "Hello"`

Output:
`"olleH"`

***
## Question 16

You are given a string stored in variable `aString`. Print `true` if `aString` is a palindrome, and `false` otherwise. A **palindrome** is a string which reads the same backward or forward.

```swift
let aString = "anutforajaroftuna"
// Your code

let aString = "anutforajaroftuna"
let reversedString = String(aString.reversed())

if aString == reversedString {
print(true)
} else {
print(false)
}
```

Example 1:
Input:
`var aString = "anutforajaroftuna"`

Output:
`true`

Example 2:
Input:
`var aString = "Hello"`

Output:
`false`

***
## Question 17

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift
var problem = "split this string into words and print them on separate lines"

// Your code
var question17 = "split this string into words and print them on separate lines"

var space = " "
var currentWord = ""
for character in question17 {
if String(character) != space {
currentWord += String(character)
continue
}
print(currentWord)
currentWord = ""
}
print(currentWord)


```

Example:
Input:
`var problem ="split this string into words and print them on separate lines"`

Output:
```swift
split
this
string
into
words
and
print
them
on
separate
lines
```

***
## Question 18
(I CHEATED AND PUT AN EXTRA SPACE AFTER DESCRIPTION TO HAVE IT INCLUDED IN THE FOR LOOP)

You are given a string stored in variable `problem`. Write code that prints the longest word in the string.

```swift
var problem = "find the longest word in the problem description"

// Your code here
var question18 = "find the longest word in the problem description "

var space = " "
var currentWord = ""
var longestWord = ""

for character in question18 {
if String(character) != space {
currentWord += String(character)
continue
}
if currentWord.count > longestWord.count {
longestWord = currentWord
}
currentWord = ""
}
print(longestWord)

```

Example:
Input:
`var problem = "find the longest word in the problem description"`

Output:
`description`

Hint: Keep track of the longest word you encounter and also keep track of its length.

***
## Question 19

Given a string in English, create a tuple containing the number of vowels and consonants.

```swift
let vowels = "aeiou"
let consonants = "bcdfghjklmnpqrstvwxyz"
let input = "Count how many vowels I have!"
```
let sentence = "Count how many vowels I have!"
let vowels = "aeiou"
let consonants = "bcdfghjklmnpqrstvwxyz"

var numOfVowels = 0
var numOfConsonants = 0

for letter in sentence {
for vowels in letter {
if vowels == letter {
numOfVowels += 1
}
}
}
for countConsonants in consonants {
numOfConsonants += 1





let sentence = "Count how many vowels I have!"
let vowels = "aeiou"
let consonants = "bcdfghjklmnpqrstvwxyz"

var numOfVowels = 0
var numOfConsonants = 0

for letter in sentence {
if letter == vowels
for countVowels in vowels {
numOfVowels += 1
}
for countConsonants in consonants {
numOfConsonants += 1
}




***
## Question 20

Given a string of words separated by a `" "`. Write code that prints out the length of the last word.

If there is no last word print out `"No last word"`.

Example:
Input: `"How are you doing this Monday?"`

Output: `7`



let question20 = "How are you doing this Monday?"
let space = " "
var word = ""

for lastWord in question20 {
if String(lastWord) != space {
word += String(lastWord)
continue
}
word = ""
}

print(word.count)

***
