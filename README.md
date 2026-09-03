## ECE2112-PA1

Made by: Geri Allison Geneta | 2ECE-B

This repository contains our Programming Assignment 1 for ECE2112. This project covers three python problems referenced to Module 1 - Base Computing with Python.

## A. Word Rotation Problem

Create a function that takes a word as an input and rotates it by shifting its first letter to the end of the string.

The following functions and methods were used in this problem:

* `len()` - a built-in function that determines the overall length of the string, which gives us the upper bound needed to slice up to the very last character.

        Example: len("Hello") --> 5

* String Slicing (`[starting index : no. of letters : increment]`) - a method used to divide the word into specific sections.
  
          Example: If text = "Hello", text[1:5:1] gives "elloH" and text[0:1:1] gives "H".

These were combined using the `+` operator to attach the initial letter to the tail of the remaining characters, forming the rotated output:

```python
text = input("Enter a word: ")
length = len(text)

def rotate_word(text):
   return (text[1:length:1]) + (text[0:1:1])

rotate_word(text)```

Output:
Enter a word:  Programming
'rogrammingP'

Examples:

rotate_word("Python") ==> 'ythonP'
rotate_word("logic") ==> 'ogicl'
rotate_word("Code") ==> 'odeC'
rotate_word("A") ==> 'A'
