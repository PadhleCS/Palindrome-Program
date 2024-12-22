# Palindrome Checker in Python

This repository contains Python programs to check whether a given string or number is a palindrome.

## What is a Palindrome?
A **palindrome** is a word, phrase, number, or other sequence of characters that reads the same forward and backward (ignoring spaces, punctuation, and capitalization). Examples include:

- "radar"
- "level"
- "12321"

## Programs Overview
This repository contains two separate programs:

1. **String Palindrome Checker**
   - Checks if a given string is a palindrome.
   - Ignores spaces, special characters, and is case-insensitive.

2. **Number Palindrome Checker**
   - Checks if a given number is a palindrome.
   - Works by converting the number into a string and comparing it in reverse.

## Program 1: Palindrome Checker for Strings

### Definition
This program checks if an input string is a palindrome by removing non-alphanumeric characters, converting it to lowercase, and comparing it with its reverse.

### Code
```python
# Palindrome Checker for Strings

def is_palindrome(s):
    s = ''.join(e for e in s if e.isalnum()).lower()
    return s == s[::-1]

# Example Usage
string = input("Enter a string: ")
if is_palindrome(string):
    print("The string is a palindrome.")
else:
    print("The string is not a palindrome.")
```

## Program 2: Palindrome Checker for Numbers

### Definition
This program checks if a given number is a palindrome by converting it to a string and comparing it with its reverse.

### Code
```python
# Palindrome Checker for Numbers

def is_palindrome_number(n):
    return str(n) == str(n)[::-1]

# Example Usage
number = int(input("Enter a number: "))
if is_palindrome_number(number):
    print("The number is a palindrome.")
else:
    print("The number is not a palindrome.")
```

## How to Run the Programs
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/palindrome-python.git
   ```
2. Navigate to the folder:
   ```bash
   cd palindrome-python
   ```
3. Run the script:
   ```bash
   python palindrome_string.py
   ```
   ```bash
   python palindrome_number.py
   ```

## Contributions
Contributions are welcome! Feel free to submit a pull request.

## License
This project is licensed under the MIT License.
