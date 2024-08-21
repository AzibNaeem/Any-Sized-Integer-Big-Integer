# BigInteger Calculator in C++

This repository contains an implementation of a `BigInteger` class in C++, which supports arithmetic operations on arbitrarily large integers. This class provides methods for addition, subtraction, multiplication, and division, allowing operations on integers larger than the built-in data types can handle.

## Features

- **Support for Large Integers:** The `BigInteger` class can handle numbers larger than the standard `int` or `long` data types.
- **Arithmetic Operations:** 
  - Addition (`+`)
  - Subtraction (`-`)
  - Multiplication (`*`)
  - Division (`/`)
- **User Interaction:** The main function includes an interactive calculator that allows users to perform operations on large integers.

## Class Overview

### Private Members

- `char *number`: A dynamic array that stores the digits of the big integer as characters.
- `int digits`: The number of digits in the big integer.
- `char sign`: Stores the sign of the number ('+' for positive, '-' for negative).

### Private Methods

- `bool greaterOrEqual(const BigInteger &num)`: Compares the current object with another `BigInteger` to determine if it is greater than or equal to the other.
- `bool IsEquals(const BigInteger &num)`: Checks if the current `BigInteger` is equal to another `BigInteger`.
- `BigInteger& operator=(const BigInteger &num)`: Overloads the assignment operator to copy another `BigInteger` object.
- `void allocateMemory(int newDigits)`: Allocates memory for the number based on the number of digits.

### Public Methods

- **Constructors:**
  - `BigInteger()`: Default constructor that initializes the object to zero.
  - `BigInteger(int num)`: Constructs a `BigInteger` from an integer.
  - `BigInteger(const char *num)`: Constructs a `BigInteger` from a string.
  - `BigInteger(const BigInteger &num)`: Copy constructor.

- **Destructor:**
  - `~BigInteger()`: Cleans up dynamically allocated memory.

- **Arithmetic Operations:**
  - `BigInteger add(BigInteger &num)`: Adds two `BigInteger` objects.
  - `BigInteger subtract(BigInteger &num)`: Subtracts one `BigInteger` from another.
  - `BigInteger multiply(BigInteger &num)`: Multiplies two `BigInteger` objects.
  - `BigInteger divide(BigInteger &num)`: Divides one `BigInteger` by another.

- **Utility Methods:**
  - `void print()`: Prints the `BigInteger` to the console.

## Main Program Overview

The main function provides an interactive console-based calculator that allows users to perform operations on large integers. The user can input expressions like `123 + 456`, and the program will output the result. The available operations include addition, subtraction, multiplication, and division.

### Menu Options

- `+` - Perform addition.
- `-` - Perform subtraction.
- `*` - Perform multiplication.
- `/` - Perform division.
- `!` - Exit the calculator.

### Example Usage

```cpp
_________________________________________Welcome to the Big Number Calculator!__________________________________________
-> What mathematical magic can I perform today?


  +. Addition Extravaganza
  -. Subtraction Showdown
  *. Multiplication Marathon
  /. Division Duel
  !. Exit the Arena

Enter your expression in the format:  number1 op number2
(e.g., 123 + 456)
Enter your expression: 12345678901234567890 + 98765432109876543210
Result = 111111111011111111100
```

## Memory Management

- The class uses dynamic memory allocation to handle the large number of digits.
- Proper memory management is ensured with a destructor that deletes allocated memory when an object goes out of scope.
- The copy constructor and assignment operator ensure deep copies of `BigInteger` objects to avoid shallow copy issues.

## Limitations

- The current implementation does not handle floating-point numbers or operations on negative numbers in division.
- Division by zero is not handled and will output an intermediate message.

## How to Compile and Run

1. Compile the code using a C++ compiler:

   ```bash
   g++ -o BigIntegerCalculator BigInteger.cpp
   ```

2. Run the compiled program:

   ```bash
   ./BigIntegerCalculator
   ```

---
