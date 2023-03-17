# TextEditor
ENGR 103 C++ Text Editor

Problem statement:
You are tasked to write a program that reads in a sentence or a paragraph (max length 1023 letters)
from the user, store it as a string, and gives the user several options for operations to perform on the text
or quit. After performing an operation, the user should be prompted to select another option until they
choose to quit. The program must handle all types of bad inputs from user and recover from the errors.
Detailed requirements for each choice are listed below:
1. Vowels vs. Consonants: Check if the number of vowels equals the number of consonants.
Ignore any nonletter characters.
Example: User enters "banana"; program prints " # vowels = # consonants."
Example: User enters "ban ana44!"; program prints " # vowels = # consonants."
Example: User enters "zip"; program prints "# vowels != # consonants."
2. Letter swap: prompt the user for two valid letters, create a copy of the original string, and
modify the copy string by replacing all occurrences of the first letter with the second letter.
Example: User enters "Off we go, into the wild blue yonder!", then characters 'o'
and 'i'. Program prints: Iff we gi, inti the wild blue yinder!
(Notice: capitalization is preserved)
3. Flip (reverse) the string: create a copy of the original string, and then reverse it.
Example: User enters "ban ana54!"; program creates a new string and outputs: "!45ana
nab"
Example: User enters "zip"; program creates a new string and outputs: "piz"
4. Palindrome Detector: Determine whether the input string is palindrome or not. A palindrome is
a word, phrase, or sequence that reads the same backwards as forward. E.g., racecar, madam.
Examples of palindromes that your code needs to detect:
User enters “11Radar911”, program outputs “This is a palindrome.” (Ignore the numbers
and case of letters)
User enters “top sports”, program outputs “This is not a palindrome.”
User enters “Was it a car or a cat I saw?”, program outputs “This is a
palindrome.” (Ignore the space and special characters, ‘?’)
5. Words frequency: Prompt the user for N words that the user wants to search for in the input
string. For this assignment, assuming N is a positive integer less than or equal to 10. Use a string
array to store N words, and output the frequency of N given words in the input string.
Example: User enters “This is a test sentence, is this?”, then 3 words, “this”,
“text”, and “test”. The program outputs:
this: 2
text: 0
test: 1
(Note: Case insensitive, meaning “word” and “WoRD” are the same; All numbers and special
characters in the string are ignored, meaning “wor32rd”, “wo]]]rd343.34”, and “word” are the
same)
Suggested functions:
a. bool is_palindrome (string str); //return true if str is palindrome, false otherwise
b. string purge_string (string str); //accepts a string, and returns a version where
all numbers, spaces, and special characters have been removed
OR you may use this:
void purge_string (string str, string& str_new); //accepts two c-strings,
remove all spaces and special characters in str, and store the new string into str_new
For frequency of given words, the N words must be entered at one time before searching to see if the
words are in the sentence/paragraph. In other words, you cannot ask for a word, search its frequency
and then ask for another word. You must ask for all words before searching for the words. 
