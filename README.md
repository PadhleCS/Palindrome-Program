# Fibonacci Series in Python

## Overview
This repository contains Python programs to generate and work with the Fibonacci series. The Fibonacci sequence is a series of numbers where each number is the sum of the two preceding ones, usually starting with 0 and 1.

## Table of Contents
1. Introduction
2. Recursive Implementation
3. Iterative Implementation
4. Optimized Implementation using Memoization
5. Example Usage
6. License

## 1. Introduction
The Fibonacci series is defined mathematically as:
```
F(n) = F(n-1) + F(n-2)
F(0) = 0, F(1) = 1
```
This repository demonstrates different approaches to implement this series in Python.

---

## 2. Recursive Implementation
```python
def fibonacci_recursive(n):
    if n <= 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fibonacci_recursive(n-1) + fibonacci_recursive(n-2)

# Example Usage
print(fibonacci_recursive(10))
```

---

## 3. Iterative Implementation
```python
def fibonacci_iterative(n):
    a, b = 0, 1
    for _ in range(n):
        a, b = b, a + b
    return a

# Example Usage
print(fibonacci_iterative(10))
```

---

## 4. Optimized Implementation using Memoization
```python
cache = {}

def fibonacci_memoization(n):
    if n in cache:
        return cache[n]
    if n <= 0:
        return 0
    elif n == 1:
        return 1
    cache[n] = fibonacci_memoization(n-1) + fibonacci_memoization(n-2)
    return cache[n]

# Example Usage
print(fibonacci_memoization(10))
```

---

## 5. Example Usage
Run any of the implementations and pass a number as an argument to get the nth Fibonacci number.

---

## 6. License
This project is licensed under the MIT License.

## Contributions
Feel free to open issues and submit pull requests if you have improvements or additional implementations!

---

## Author
Padhle CS
