---
layout: default
---

![SwiftierSwift](//raw.githubusercontent.com/omaralbeik/SwiftierSwift/master/logo.png)

*A handy collection of native Swift 3 extensions to boost your productivity.*

[SwiftierSwift](//github.com/OmarAlbeik/SwiftierSwift) is a Swift3 library with various extensions done to make iOS application development easier and readable for everyone

## How to use?

Copy to the extensions folder of your Xcode project to use all extensions, or a specific extension.

## Notes on docs:

We also included inline documentation to you to easily look up things in auto completion while typing, making you write code faster.

## Show me some examples

#### Array Extensions (14)
```swift
// Remove duplicates from array
[1, 2, 3, 1, 3].removeDuplicates() -> [1, 2, 3]

// Return all indexes of specified item
["h", "e", "l", "l", "o"].indexes(of item: "l") -> [2, 3]

// Return random item from array
[1, 2, 3, 4, 5].randomItem -> 3

// and many others!
```


#### Date Extensions (23)
```swift
// Get and set components from date with ease
date.hour = 14

// Check if date is in today
Date().isInToday -> true

// Add 1 month to current date
Date().add(component: .month, value: 1)

// Return beginning of current day
Date().beginning(of component: .day)

// Check if date is in current calendar unit
Date().isIn(current: .month) -> true

// Return iso8601 string for date
Date().iso8601String -> "2016-08-23T21:26:15.287Z"

// Create date from iso8601 string
let date = Date(iso8601String: "2016-08-23T21:26:15.287Z")

// and many others!
```


#### String Extensions (48)
```swift
// Return count of substring in string
"hello world".count(of "o", caseSensitive: false) -> 2

// Return an array of strings separated by given string
"hello world".split(by separator: " ") -> ["hello", "world"]

// Return string with no spaces or new lines in beginning and end
"\n Hello   ".trimmed -> "Hello"

// Return most common character in string
"swifterSwift is making swift more swifty".mostCommonCharacter -> "i"

// Returns CamelCase of string
"Some variable name".camelCased -> "someVariableName"

// Check if string is in valid email format
"omaralbeik@gmail.com".isEmail -> true

// Check if string contains at least one letter and one number
"123abc".isAlphaNumeric -> true

// Reverse string
"123abc".reverse() -> "cba321"

// Return latinized string
"Hèllö Wórld!".latinize() -> "Hello World!"

// Return latinized string
String.random(of length: 10) -> "AhEju28kNl"

// Check if string contains one or more instance of substring
"Hello World!".contain(string: "o", caseSensitive: false) -> true

// Check if string contains one or more emojis
"string👨‍with😍emojis✊🏿".containEmoji -> true

// Convert string to numbers
"12.12".toDouble -> 12.12

// Encode string into url
"it's easy to encode strings".urlEncoded() -> "it's%20easy%20to%20encode%20strings"

// Decode url
"it's%20easy%20to%20encode%20strings".urlDecoded() -> "it's easy to encode strings"

// Repeat a string n times
"s" * 5 -> "sssss"
// and many others!
```


#### UIColor Extensions (7)
```swift
// Create new UIColor for RGB values
let color = UIColor(red: 121, green: 220, blue: 164)

// Create new UIColor for a hexadecimal value
let color = UIColor(netHex:0x45C91B)

// Return hexadecimal value string
UIColor.red.hexString -> "#FF0000"

// Return brand colors from more than 30 social brands
let facebookColor = UIColor.socialColors.facebook

// and many others!
```


#### Number Extensions (33)
```swift
// Return square root of a number
√ 9 = 3

// Return square power of a number
5 ^ 2 = 25

// Return a number plus or minus another number
5 ± 2 = (3, 7)

// Return random number in range
Int.randomBetween(min: 1, max: 10) = 6

// Return roman numeral for a number
134.romanNumeral = "CXXXIV"

// and many others!
```


#### Misc Extensions
```swift
// Return JSON string from a dictionary
let jsonString = someDictionary.jsonString(prettify: true)

// Return JSON data from a dictionary
let jsonData = someDictionary.jsonData

// Check if app is running in debugging mode
swifterSwift.isInDebuggingMode

// Check if app is running on simulator
swifterSwift.isRunningOnSimulator

// and many others!
```


## Author

Omar Albeik
/ [Twitter](//twitter.com/OmarAlbeik)
/ [Github](//github.com/OmarAlbeik)

## Contributors

Eng. Abdul Rahman Dabbour
/ [Github](//github.com/thedabbour)

Mert Akengin
/ [Twitter](//twitter.com/PvtMert)
/ [Github](//github.com/PvtMert)

<!-- yes we stole it from somewhere else -->
<a href="//github.com/OmarAlbeik/SwiftierSwift" class="github-corner"><svg width="80" height="80" viewBox="0 0 250 250" style="fill:#151513; color:#fff; position: absolute; top: 0; border: 0; right: 0;"><path d="M0,0 L115,115 L130,115 L142,142 L250,250 L250,0 Z"></path><path d="M128.3,109.0 C113.8,99.7 119.0,89.6 119.0,89.6 C122.0,82.7 120.5,78.6 120.5,78.6 C119.2,72.0 123.4,76.3 123.4,76.3 C127.3,80.9 125.5,87.3 125.5,87.3 C122.9,97.6 130.6,101.9 134.4,103.2" fill="currentColor" style="transform-origin: 130px 106px;" class="octo-arm"></path><path d="M115.0,115.0 C114.9,115.1 118.7,116.5 119.8,115.4 L133.7,101.6 C136.9,99.2 139.9,98.4 142.2,98.6 C133.8,88.0 127.5,74.4 143.8,58.0 C148.5,53.4 154.0,51.2 159.7,51.0 C160.3,49.4 163.2,43.6 171.4,40.1 C171.4,40.1 176.1,42.5 178.8,56.2 C183.1,58.6 187.2,61.8 190.9,65.4 C194.5,69.0 197.7,73.2 200.1,77.6 C213.8,80.2 216.3,84.9 216.3,84.9 C212.7,93.1 206.9,96.0 205.4,96.6 C205.1,102.4 203.0,107.8 198.3,112.5 C181.9,128.9 168.3,122.5 157.7,114.1 C157.9,116.9 156.7,120.9 152.7,124.9 L141.0,136.5 C139.8,137.7 141.6,141.9 141.8,141.8 Z" fill="currentColor" class="octo-body"></path></svg></a><style>.github-corner:hover .octo-arm{animation:octocat-wave 560ms ease-in-out}@keyframes octocat-wave{0%,100%{transform:rotate(0)}20%,60%{transform:rotate(-25deg)}40%,80%{transform:rotate(10deg)}}@media (max-width:500px){.github-corner:hover .octo-arm{animation:none}.github-corner .octo-arm{animation:octocat-wave 560ms ease-in-out}}</style>
