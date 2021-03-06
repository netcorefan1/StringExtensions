(This is a port of the StringExtensions library published to codeplex before- now targeting .NET Standard 1.0)

# Intro
By default, the .NET BCL introduces a set of static methods and instance members for the String type that gives us basic support for common string operations. Unfortunately, the methods offered are incomplete. Methods like Contains and Replace provide no mechanism whatsoever for explicitly setting the comparison type. Try and replace a word within a string with another word while not caring about capitals and share the pain.

Alternatively, there are loads of cases where custom solutions are provided for string functionality that could and arguably should be functionality of a naked string class. Most of the times, the custom implementations are not well tested and/or documented.
# Goal
The String Extensions project aims to provide a more complete String type experience by adding extension methods (including overloads of existing methods) providing commonly required functionality in a well-tested and well-documented fashion.
We have a clear name and flexible deployment (binary release including nu-get package for multiple platforms).

# Solution
Below you'll find the summary of all methods currently supported. More coming soon! Each method comes with code contracts and Microsoft Pex unit tests. (Yes, if you want to know, we got 100% code coverage).

- [AllBetween](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/AllBetween.cs) Extracts all encounters of strings between outer enclosures **5 overloads**
- [Between](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/Between.cs) Extracts the first encounter of a string between outer enclosures **5 overloads**
- [Contains](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/Contains.cs) Determines whether a string contains the token specified **2 overloads**
- [CountSubstring](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/CountSubstring.cs) Counts the total amount of occurrences of a token within a string **3 overloads**
- [CountSubstringStart](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/CountSubstringStart.cs) Counts the total amount of occurrences of a token at the start of a string **2 overloads**
- [CountSubstringEnd](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/CountSubstringEnd.cs) Counts the total amount of occurrences of a token at the end of a string **2 overloads**
- [Convert](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/Convert.cs) Converts the string given to another encoding **2 overloads**
- [IsEmpty](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/IsEmpty.cs) Determines whether the string given is empty (no content) **1 overload**
- [IsEmptyOrWhitespace](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/IsEmptyOrWhiteSpace.cs) 1 overload Determines whether the string given is empty or contains only white spaces **1 overload**
- [Left](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/Left.cs) Extracts a certain amount of characters from the left side of a string **1 overload**
- [LeftOf](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/LeftOf.cs) Extracts all characters from the left side of a string limited by a certain occurrence of a token **5 overloads**
- [LeftOfLast](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/LeftOfLast.cs) Extracts all characters from the left side of a string limited by a the last occurrence of a token **3 overloads**
- [Right](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/Right.cs) Extracts a certain amount of characters from the right side of a string **1 overload**
- [RightOf](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/RightOf.cs) Extracts all characters from the right side of a string limited by a certain occurrence of a token **5 overloads**
- [RightOfLast](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/RightOfLast.cs) Extracts all characters from the right side of a string limited by the last occurrence of a token **3 overloads**
- [Replace](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/Replace.cs) Replaces occurrences of a specified string with another specified string **3 overloads**
- [Reverse](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/Reverse.cs) Reverses all characters within a certain range within a string **2 overloads**
- [Size](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/Size.cs) Calculates the total amount of bytes occupied by a given string **2 overloads**
- [SizeAs](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/SizeAs.cs) Calculates the total amount of bytes occupied by a given string when it would be converted to a certain encoding (e.g. useful for testing database limits) **2 overloads**
- [TrimStart](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/TrimStart.cs) Trims occurrences of token from the start of a string **4 overloads**
- [TrimStartOnce](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/TrimStartOnce.cs) Trims the first occurrence of token from the start of a string **2 overloads**
- [TrimEnd](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/TrimEnd.cs) Trims occurrences of token from the end of a string **4 overloads**
- [TrimEndOnce](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/TrimEndOnce.cs) Trims the first occurrence of token from the end of a string **2 overloads**
- [Truncate](https://github.com/kbekkenutte/StringExtensions/blob/master/tests/StringExtensions.Examples/Truncate.cs) Truncates a string until a maximum length and possibly adds an ellipsis. This method also deals with boundaries **3 overloads**
