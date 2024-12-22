# Armstrong Number Program

This repository contains Python programs to determine whether a given number is an Armstrong number.

## What is an Armstrong Number?
An **Armstrong number** (also known as a **narcissistic number**) is a number that is equal to the sum of its digits each raised to the power of the number of digits.

### Example:
- 153 → 1³ + 5³ + 3³ = 153 (Armstrong Number)
- 9474 → 9⁴ + 4⁴ + 7⁴ + 4⁴ = 9474 (Armstrong Number)
- 123 → 1³ + 2³ + 3³ ≠ 123 (Not an Armstrong Number)

## Program Overview
This program:
- Takes an integer input from the user.
- Calculates if the given number is an Armstrong number.
- Prints whether the number is an Armstrong number or not.

## Code Implementation
```python
# Program to check if a number is an Armstrong number

def is_armstrong(number: int) -> bool:
    num_str = str(number)
    num_digits = len(num_str)
    return number == sum(int(digit) ** num_digits for digit in num_str)

# User input
if __name__ == '__main__':
    try:
        num = int(input("Enter a number: "))
        if is_armstrong(num):
            print(f"{num} is an Armstrong number.")
        else:
            print(f"{num} is not an Armstrong number.")
    except ValueError:
        print("Please enter a valid integer.")
```

## How to Run the Program
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/armstrong_number_python.git
   ```
2. Navigate to the directory:
   ```bash
   cd armstrong_number_python
   ```
3. Run the program:
   ```bash
   python armstrong.py
   ```

## Test Cases
| Input | Output |
|-------|--------|
| 153   | Armstrong Number |
| 9474  | Armstrong Number |
| 123   | Not an Armstrong Number |

## License
This project is licensed under the MIT License.
