# Inverted Triangle Number Pattern in Java

## Description
This Java program prints an inverted triangle number pattern based on user input. The user specifies the size of the pattern, and the program generates a symmetric number pattern with decreasing rows. The pattern follows a structured approach where numbers increase towards the center and then decrease symmetrically.

## Pattern Example
For an input `n = 5`, the output will be:
```
123454321
 1234321
  12321
   121
    1
```

## Code Implementation
```java
package number_patterns;

import java.util.Scanner;

public class Inverted_Triangle
{
    public static void main(String[] args)
    {
        Scanner s = new Scanner(System.in); // Creating Scanner object to take user input
        System.out.println("Enter the size");
        int n = s.nextInt(); // Reading user input

        for(int i = 1; i <= n; i++) // Outer loop for rows
        {
            int num = 1; // Variable to track numbers in pattern

            for(int j = 1; j <= i; j++) // Loop for leading spaces
            {
                System.out.print(" ");
            }
            
            for(int j = i; j < n; j++) // Loop for increasing numbers
            {
                System.out.print(num++);
            }
            
            for(int j = i; j <= n; j++) // Loop for decreasing numbers
            {
                System.out.print(num--);
            }
            
            System.out.println(); // Move to the next line
        }
    }
}
```

## Explanation of the Code

### 1. **Scanner Class**
- The `Scanner` class is used to take user input from the console.
- We create a `Scanner` object `s` using `new Scanner(System.in)`.
- The method `s.nextInt()` reads an integer input from the user and stores it in variable `n`.

### 2. **Variables**
- `n`: Stores the user-input size of the pattern.
- `num`: Used to generate the sequence of increasing and decreasing numbers.

### 3. **For Loops**
- **Outer loop (`for(int i = 1; i <= n; i++)`)**: Controls the number of rows in the pattern.
- **First inner loop (`for(int j = 1; j <= i; j++)`)**: Prints leading spaces to align the pattern.
- **Second inner loop (`for(int j = i; j < n; j++)`)**: Prints increasing numbers from `1` to `n-i`.
- **Third inner loop (`for(int j = i; j <= n; j++)`)**: Prints decreasing numbers to create a symmetric effect.
- `System.out.println();` moves the cursor to the next line after completing a row.

## How the Pattern Works
1. The first row starts at the leftmost position with numbers increasing and then decreasing symmetrically.
2. Each subsequent row has one more leading space than the previous row.
3. The number of digits decreases as we go downward, forming an inverted triangle.

## Example Execution
**Input:**
```
Enter the size
5
```
**Output:**
```
123454321
 1234321
  12321
   121
    1
```

## Conclusion
This program effectively demonstrates nested loops, pattern printing, and user input handling in Java. The structured approach of loops ensures the correct alignment and symmetry of numbers in the pattern.

## Clone
```
git clone https://github.com/Ananthadatta02/Java-Inverted_Triangle.git
```
