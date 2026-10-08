# Java Recursive Product

A Java console application developed for a Programming II coursework assignment at Colorado State University Global. The project demonstrates recursion and iteration by calculating the product of five integers entered by the user.

The application uses two different algorithms to perform the same calculation, allowing their results and approaches to be compared.

## Project Overview

The program prompts the user to enter five integers and stores them in an array.

It then calculates the product of those integers using two methods:

1. **Recursive multiplication** — A method that calls itself to process the array.
2. **Iterative multiplication** — A method that uses a `for` loop to process the array.

Both results are displayed in the console.

This project demonstrates how the same programming problem can be solved using different control structures.

## Features

- Collects five integers through console input
- Stores user input in an integer array
- Calculates the product using recursion
- Calculates the product using iteration
- Demonstrates a recursive base case
- Uses an enhanced comparison of two algorithmic approaches
- Displays both calculated results
- Uses Java's `Scanner` class for keyboard input

## Technologies Used

- **Java** — Application logic and mathematical operations
- **Java Scanner** — Console input handling
- **Arrays** — Storage of user-entered integers
- **Recursion** — Repeated method calls to process array elements
- **Iteration** — Loop-based multiplication

No external libraries are required.

## Programming Concepts Demonstrated

### Recursion

Recursion occurs when a method calls itself to solve a smaller part of a problem.

The application implements the following recursive method:

```java
public static int recursiveProduct(int[] numbers, int index)
{
    // Base case stops recursion
    if(index == numbers.length - 1)
    {
        return numbers[index];
    }

    // Recursive case multiplies numbers
    return numbers[index] * recursiveProduct(numbers, index + 1);
}
```

The method accepts two parameters:

- `numbers` — The array containing the integers.
- `index` — The current position in the array.

The method multiplies the current array element by the result of a recursive call using the next index.

### Recursive Base Case

Every recursive method needs a condition that stops additional recursive calls.

In this application, the base case is:

```java
if(index == numbers.length - 1)
{
    return numbers[index];
}
```

When the method reaches the final array element, it returns that value instead of calling itself again.

The previous recursive calls then return their multiplication results until the original method call completes.

### Iteration

The program also includes an iterative method that performs the same calculation using a `for` loop:

```java
public static int iterativeProduct(int[] numbers)
{
    int product = 1;

    for (int i = 0; i < numbers.length; i++)
    {
        product = product * numbers[i];
    }

    return product;
}
```

The method begins with a product of `1` and multiplies each array element into the running total.

Unlike recursion, iteration repeats operations through a loop rather than additional method calls.

### Arrays

The application creates an integer array containing five elements:

```java
int[] numbers = new int[5];
```

A `for` loop collects the user's input and stores each value in the array.

The same array is then passed to both multiplication methods.

### Comparing Recursion and Iteration

| Concept | Recursive Method | Iterative Method |
|---------|------------------|------------------|
| Approach | Calls itself | Uses a loop |
| Stopping condition | Base case | Loop condition |
| Processing | One array element per call | One array element per iteration |
| Result | Product of all five integers | Product of all five integers |
| Additional method calls | Yes | No |

Both methods calculate the same mathematical result when the product fits within Java's `int` range.

For this assignment, recursion provides practice with method calls and base cases, while iteration demonstrates an alternative solution using familiar loop structures.

## Project Structure

```text
java-recursive-product/
├── src/
│   └── RecursiveProduct.java
├── .gitignore
├── LICENSE
└── README.md
```

### Source File

**`RecursiveProduct.java`**

Contains the complete application, including:

- The `main()` method
- Console input collection
- Integer array initialization
- Recursive multiplication method
- Iterative multiplication method
- Console output

The original assignment pseudocode and source-code comments have been preserved.

## How to Run

### Requirements

- Java Development Kit (JDK)
- Terminal or command prompt

### Instructions

1. Clone or download the repository.

2. Open a terminal in the repository's root directory.

3. Compile the Java source file:

   ```bash
   javac src/RecursiveProduct.java
   ```

4. Run the application:

   ```bash
   java -cp src RecursiveProduct
   ```

5. Enter five integers when prompted.

6. The application displays the recursive and iterative products.

## Example Output

Example using the integers `2`, `3`, `4`, `5`, and `6`:

```text
Enter number 1: 2
Enter number 2: 3
Enter number 3: 4
Enter number 4: 5
Enter number 5: 6

Recursive product: 720
Iterative product: 720
```

Both methods return the same result:

```text
2 × 3 × 4 × 5 × 6 = 720
```

## Testing

The application can be tested using different combinations of integers.

| Test Case | Input Values | Expected Product |
|-----------|--------------|------------------|
| Positive integers | 2, 3, 4, 5, 6 | 720 |
| Includes zero | 2, 3, 0, 5, 6 | 0 |
| One negative integer | -2, 3, 4, 5, 6 | -720 |
| Two negative integers | -2, -3, 4, 5, 6 | 720 |
| All ones | 1, 1, 1, 1, 1 | 1 |

These test cases help demonstrate that the two methods produce equivalent results for different combinations of valid integers.

## Current Limitations

This project was developed as an introductory programming assignment and has several limitations:

- The application requires exactly five integers.
- Input must consist of valid integer values.
- Non-integer input is not handled through custom validation.
- The recursive method assumes the array contains at least one element.
- Multiplication uses Java's `int` data type, which can overflow when the product exceeds its supported range.
- Results are displayed in the console rather than saved to a file.

These limitations reflect the educational scope of the original assignment.

## Educational Context

This application was developed for a Programming II course at Colorado State University Global.

The assignment provided practical experience with:

- Understanding recursive method calls
- Defining and using a recursive base case
- Comparing recursion and iteration
- Creating and processing arrays
- Passing arrays as method parameters
- Collecting console input using `Scanner`
- Working with integer arithmetic
- Organizing calculations into reusable methods
- Testing algorithms using different values

The original coursework structure and pseudocode have been preserved to demonstrate programming progression throughout the degree program.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
