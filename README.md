# Strings Lab 2

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.

## Question 1

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift
var problem = "split this string into words and print them on separate lines"
var problemArr = problem.split(separator: " ")

for i in problemArr {
    print(i)
}
```




## Question 2

Given a string `testString` create a new variable called `condensedString` that has any consecutive spaces in `testString` replaced with a single space.

```swift
let testString = "  How   about      thesespaces  ?  "
//condensedString = " How about thesespaces ? "
```


## Question 3

Given a string with multiple words. Reverse the string word by word.
```swift 
let aString: String = "Swift is the best language"
let aStringArr = aString.split(separator: " ")
var reverse = (aStringArr.reversed())
for word in reverse {
print(word, terminator: " " )
}


```


## Question 4

Given a string with multiple words. Write code that prints how many of them are palindromes.

```swift 
var aString = "danaerys dad cat civic bottle"
let aStringArr = aString.split(separator: " ")

var reverse = String(aString.reversed())
let reverseArr = reverse.split(separator: " ")

var pallindromeCount = 0


for word in aStringArr{
for word2 in reverseArr {
if word == word2  {
pallindromeCount += 1

}
}

}
print(pallindromeCount)



```


## Question 5

You are given a string representing an **attendance record** for a student. The record only contains the following three characters:

`'A' : Absent.`

`'L' : Late.`

`'P' : Present.`

If a student has more than one 'A' or more than 2 continuous 'L's that student should not be rewarded. Print true if student is to be rewarded and False if they shouldn't.

Example:

Sample Input: `"PPALLP"`

Sample Output: `true` 

```swift 
var studentRecord = "PPALLP"
var absentNum = 0
var lateNum = 0

for letter in studentRecord {
if letter == "A"{
absentNum += 1
}
}
if studentRecord.contains("LLL") || absentNum > 1{
print(false)

} else {
print(true)
}



```


## Question 6

Given a tuple with two strings. The first string is a **ransom note**, the second string being the characters from a magazine. Determine whether or not you can construct the ransom note using the characters from the magazine.

Each letter from the magazine can only be used once. You can assume all letters are lowercased.

Examples:

Sample Input1: `("a", "b")`

Sample Output1: `False`

Sample Input2: `("aa", "aab")`

Sample Output2: `True` 
```swift 
var input2 = (ransom:"aa", magazine:"aba")
var check = String(input2.magazine.sorted()).contains(String(input2.ransom.sorted()))

```
