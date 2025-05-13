# EX-21-POINTERS
## AIM:
Write a C program to convert a 23.65 into 25 using pointer

## ALGORITHM:
1.	Declare a double variable to hold the floating-point number (23.65).
2.	Declare a pointer to double to point to the address of the variable.
3.	Use the pointer to modify the value to 25.0.
4.	Print the modified value.
## PROGRAM:
```
#include <stdio.h>

int main() {
    float num = 23.65;
    float *ptr = &num;

    // Output original value
    printf("Original value: %.2f\n", num);

    // Modify value using pointer
    *ptr = 25;

    // Output modified value
    printf("Modified value: %.2f\n", num);

    return 0;
}

```
## OUTPUT:
![m5 1](https://github.com/user-attachments/assets/ad474006-f363-4765-9344-07962b7f075a)

 	
## RESULT:
Thus the program to convert a 23.65 into 25 using pointer has been executed successfully.
 
 


# EX-22-FUNCTIONS AND STORAGE CLASS

## AIM:

Write a C program to calculate the Product of first 12 natural numbers using Recursion

## ALGORITHM:

1.	Define a recursive function calculateProduct that takes an integer parameter n.
2.	Return n multiplied by the result of the calculateProduct function called with n - 1.
3.	Declare an integer variable n and an unsigned long long variable product.
4.	Initialize n with the value 12 (for the first 12 natural numbers).
5.	Call the calculateProduct function with n and store the result in the product variable.
6.	Print the result, indicating it is the product of the first 12 natural numbers.

## PROGRAM:
```
#include <stdio.h>

// Recursive function to calculate factorial
long long int factorial(int n) {
    if (n == 1)
        return 1;
    else
        return n * factorial(n - 1);
}

int main() {
    int num = 12;
    long long int product;

    product = factorial(num);

    printf("Product of first 12 natural numbers (12!) is: %lld\n", product);

    return 0;
}
```
## OUTPUT:
![m5 2](https://github.com/user-attachments/assets/fd88ebd4-b555-4a14-bdcc-b832819558fb)

## RESULT:

Thus the program has been executed successfully.
 
 


# EX-23-ARRAYS AND ITS OPERATIONS

## AIM:

Write C Program to find Sum of each row of a Matrix

## ALGORITHM:

1.	Declare and initialize the matrix with the desired values.
2.	Create a loop to iterate through each row of the matrix.
3.	Inside the loop, calculate the sum of the elements in each row.
4.	Print the sum for each row.

## PROGRAM:
```
#include <stdio.h>

int main() {
    int rows, cols;

    // Input number of rows and columns
    printf("Enter number of rows: ");
    scanf("%d", &rows);

    printf("Enter number of columns: ");
    scanf("%d", &cols);

    int matrix[rows][cols];

    // Input elements of matrix
    printf("Enter elements of the matrix:\n");
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            scanf("%d", &matrix[i][j]);
        }
    }

    // Calculating sum of each row
    for (int i = 0; i < rows; i++) {
        int sum = 0;
        for (int j = 0; j < cols; j++) {
            sum += matrix[i][j];
        }
        printf("Sum of row %d = %d\n", i + 1, sum);
    }

    return 0;
}
```
## OUTPUT:
![m5 3](https://github.com/user-attachments/assets/4d0381b8-2ec4-42b1-b373-d106e2766e54)

 ## RESULT:
 Thus the C Program to Sum of each row of a Matrix executed succesfully


# EX-24-STRINGS

## AIM:

Write C program for the below pyramid string pattern. Enter a string: PROGRAM Enter number of rows: 5 P R O G R A M P R O G R A M P R O G R A M

## ALGORITHM:

1.	Input the number of rows for the pyramid (e.g., num_rows).
2.	Initialize variables:i for the row count (starting from 1),j for the character count (starting from 1)
3.	Start a loop for i from 1 to num_rows (for each row of the pyramid).
4.	Calculate the midpoint position as midpoint = (2 * num_rows - 1) / 2.
5.	End the program.

## PROGRAM:
```
#include <stdio.h>
#include <string.h>

int main() {
    char str[100];
    int rows;

    // Input string
    printf("Enter a string: ");
    scanf("%s", str);

    // Input number of rows
    printf("Enter number of rows: ");
    scanf("%d", &rows);

    // Print the pyramid pattern
    for (int i = 1; i <= rows; i++) {
        for (int j = 0; j < i; j++) {
            printf("%s ", str);
        }
        printf("\n");
    }

    return 0;
}
```
 ## OUTPUT:
 ![m5 4](https://github.com/user-attachments/assets/1e83bde8-a37b-41dc-a29a-5ad892946ad5)
 
## RESULT:

Thus the C program to String process executed successfully
 





# EX -25 –DISPLAYING ARRAYS USING POINTERS
## AIM

Write a c program to read and display an array of any 6 integer elements using pointer

## ALGORITHM
Step 1: Start the program.
Step 2: Declare the following:
•	Integer variable i for iteration.
•	Integer variable n to store the number of elements.
•	Integer array arr[10] to hold up to 10 elements.
•	Integer pointer parr and initialize it to point to the array arr.
Step 3: Read the value of n (number of elements) from the user.
Step 4: Loop from i = 0 to i < n:
•	Read an integer value and store it in the address parr + i using pointer arithmetic.
Step 5: Loop from i = 0 to i < n:
•	Print the element at *(parr + i) using pointer dereferencing.
Step 6: End the program.

## PROGRAM:
```
#include <stdio.h>

int main() {
    int arr[6];
    int *ptr;

    ptr = arr;  // Point to the beginning of the array

    // Reading array elements using pointer
    printf("Enter 6 integer elements:\n");
    for (int i = 0; i < 6; i++) {
        scanf("%d", ptr + i);  // Equivalent to &arr[i]
    }

    // Displaying array elements using pointer
    printf("The elements of the array are:\n");
    for (int i = 0; i < 6; i++) {
        printf("%d ", *(ptr + i));  // Equivalent to arr[i]
    }

    printf("\n");

    return 0;
}

```
## OUTPUT:
![m5 5](https://github.com/user-attachments/assets/19e52743-2686-40dc-9ce0-dce7a9be3b49)


## RESULT

Thus the C program to read and display an array of any 6 integer elements using pointer has been executed


