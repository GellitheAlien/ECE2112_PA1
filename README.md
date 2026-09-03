# ECE2112-PA1

Made by: Geri Allison Geneta | 2ECE-B

This repository contains our Programming Assignment 1 for ECE2112. This project covers three python problems referenced to Module 1 - Base Computing with Python.

# A. Word Rotation Problem

Create a function that takes a word as an input and rotates it by shifting its first letter to the end of the string.

The following functions and methods were used in this problem:

* len() - a built-in function that determines the overall length of the string, which gives us the upper bound needed to slice up to the very last character.

        Example: len("Hello") --> 5

* String Slicing ([starting index : no. of letters : increment]) - a method used to divide the word into specific sections.

          Example: If text = "Hello", text[1:5:1] gives "ello" and text[0:1:1] gives "H".

These were combined using the + operator to attach the initial letter to the tail of the remaining characters, forming the rotated output:

```python
text = input("Enter a word: ")
length = len(text)

def rotate_word(text):
   return (text[1:length:1]) + (text[0:1:1])

rotate_word(text)
```

    Examples:

```python
rotate_word("Python")
```

Output:
```text
'ythonP'
```

```python
rotate_word("logic")
```

Output:
```text
'ogicl'
```

```python
rotate_word("Code")
```

Output:
```text
'odeC'
```

```python
rotate_word("A")
```

Output:
```text
'A'
```

# B. Username Builder Problem

Create a function that generates a standard username format (firstname.lastname) by accepting a user's first and last name, converting them to lowercase, and removing spaces.

The following functions and methods were used in this problem:

* .lower() - a string method that converts all uppercase characters in a string into lowercase letters to keep the username uniform.

        Example: "James".lower() --> "james"

* .replace() - a string method used here to substitute space characters " " with an empty string "", so no spaces remain in the final name strings.

          Example: "ja me s".replace(" ", "") --> "james"

These operations were applied to both inputs and joined together using string concatenation with a dot "." separator:

```python
first_name = input("Enter First Name: ")
last_name = input("Enter Last Name: ")

def make_username(first_name, last_name):

    lower_first_name = first_name.lower()

    lower_last_name = last_name.lower()

    spaceless_first_name = lower_first_name.replace(" ","")

    spaceless_last_name = lower_last_name.replace(" ","")

    username = spaceless_first_name + "." + spaceless_last_name

    print(username)

make_username(first_name, last_name)
```

    Examples:

```python
make_username("Ada", "Lovelace")
```

Output:
```text
ada.lovelace
```

```python
make_username("Alan", "Turing")
```

Output:
```text
alan.turing
```

```python
make_username("Ana Maria", "De Leon")
```

Output:
```text
anamaria.deleon
```

# C. Bookend Swap Problem

Create a function that takes a sequence of elements from the user, swaps the positions of the first and last elements, and keeps all middle elements in the same position.

The following functions and methods were used in this problem:

* .split() - a string method that breaks a continuous string into a list of individual substring items based on spaces.

          Example: "1 2 3 4 5".split() --> ['1', '2', '3', '4', '5']

* Extended Sequence Unpacking (*) - an unpacking syntax where first, *middle, last = items automatically assigns the first item to first, the final item to last, and packs every element in between into a list named middle.

          Example: first, *middle, last = ['1', '2', '3', '4', '5'] assigns first = '1', middle = ['2', '3', '4'], and last = '5'.

An if-else statement combined with len() ensures that the input contains at least two items before swapping:

```python
def swap_bookends(items):

    first, *middle, last = items
    return [last] + middle + [first]

listed_items = input("Enter items seperated by spaces: ").split()

if len(listed_items) < 2:
        print("Please input 2 or more items")
else:
        print("Swapped list: " , swap_bookends(listed_items))
```

        Examples:

```python
swap_bookends([1, 2, 3, 4, 5, 6])
```

Output:
```text
[6, 2, 3, 4, 5, 1]
```

```python
swap_bookends(["red", "green", "blue"])
```

Output:
```text
['blue', 'green', 'red']
```

```python
swap_bookends([8, 3])
```

Output:
```text
[3, 8]
```

The End.

# Thank you for Reading!
