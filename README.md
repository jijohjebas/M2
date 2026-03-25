# EX-06 - Looping
## AIM:
Write a C program to print even numbers ranging from M to N (including M and N values).

## ALGORITHM:
1.	Declare two integer variables to store the values of M and N.
2.	Use the printf function to prompt the user to enter the values of M and N.
3.	Use the scanf function to read the values of M and N from the user.
4.	Use a loop (for or while) to iterate from M to N.
5.	Inside the loop, check if the current number is even.
6.	If the current number is even, print it.
7.	Continue the loop until you have iterated through all numbers from M to N.

## PROGRAM:
```
#include <stdio.h>

int main() {
  
    int M, N, i;

    printf("Enter the starting value (M): ");
    scanf("%d", &M);
    printf("Enter the ending value (N): ");
    scanf("%d", &N);

    printf("\nEven numbers between %d and %d are:\n", M, N);

    for (i = M; i <= N; i++) {
        if (i % 2 == 0) {
            printf("%d ", i);
        }

    }

    printf("\n");
    return 0;
}
```
## OUTPUT:
<img width="1219" height="514" alt="image" src="https://github.com/user-attachments/assets/e9f65b63-dbce-4d37-9cba-9a35331ebd20" />


## RESULT:
Thus the program to print even numbers ranging from M to N (including M and N values) has been executed successfully
 
 


# EX-07-Nested-loop

## AIM:

Write a C program to print the given triangular pattern using loop.

## ALGORITHM:

1.	Declare a variable to store the number of rows in the triangle.
2.	Use the printf function to prompt the user to enter the number of rows.
3.	Use a loop (for or while) to iterate through each row.
4.	Inside the loop, use another loop to print the desired number of asterisks for each row.
5.	Continue the loop until you have printed the entire triangular pattern.

## PROGRAM:
```
#include <stdio.h>

int main() {
    int rows, i, j;
    printf("Enter the number of rows: ");
    scanf("%d", &rows);

    for (i = 1; i <= rows; i++) {

        for (j = 1; j <= i; j++) {
            printf("* ");
        }
        printf("\n");
    }

    return 0;
}
```

## OUTPUT:

<img width="1192" height="395" alt="image" src="https://github.com/user-attachments/assets/5db27998-51ef-4bf4-853d-197370b7d06b" />




## RESULT:

Thus the program to print the given triangular pattern using loop has been executed successfully
 
 


# EX-08-Functions

## AIM:

Write a C program to perform addition and subtraction of two numbers using functions (with argument and without return type).

## ALGORITHM:

1.	Declare two functions, one for addition and one for subtraction. Both functions should take two integer arguments.
2.	Inside the addition & subtraction function, add & subtract the two numbers and print the result.
3.	In the main function, declare two integer variables and read their values from the user.
4.	Call the addition and subtraction functions, passing the two numbers as arguments.

## PROGRAM:
```
#include <stdio.h>

void add(int x, int y);
void subtract(int x, int y);

int main() {
    int num1, num2;

    printf("Enter two integers: ");
    scanf("%d %d", &num1, &num2);

    add(num1, num2);
    subtract(num1, num2);

    return 0;
}

void add(int x, int y) {
    int sum = x + y;
    printf("Addition: %d + %d = %d\n", x, y, sum);
}

void subtract(int x, int y) {
    int diff = x - y;
    printf("Subtraction: %d - %d = %d\n", x, y, diff);
}
```

## OUTPUT:



<img width="1164" height="588" alt="image" src="https://github.com/user-attachments/assets/e56f1b39-734a-49b3-8ac4-3d7c483faf6c" />



## RESULT:

Thus the program to perform addition and subtraction of two numbers using functions has been executed successfully
 
 


# EX-09-Use For Loop

## AIM:

Write a c program to find the sum of odd digits using for loop

## ALGORITHM:

1.	Declare variables to store the input number and the sum of odd digits.
2.	Initialize the sum of odd digits to 0.
3.	Use a for loop to iterate through each digit of the input number.
4.	Inside the loop, extract the rightmost digit of the number (using the modulo operator % and division by 10).
5.	If the digit is odd, add it to the sum of odd digits.
6.	Print the sum of odd digits.

## PROGRAM:
```
#include <stdio.h>

int main() {
    int num, temp, digit;
    int sum = 0;

    printf("Enter an integer: ");
    scanf("%d", &num);
    temp = num;
    for (temp = num; temp != 0; temp = temp / 10) {
        digit = temp % 10;
        if (digit % 2 != 0) {
            sum = sum + digit;
        }
    }
    printf("The sum of odd digits in %d is: %d\n", num, sum);

    return 0;
}
```

## OUTPUT:

<img width="1162" height="428" alt="image" src="https://github.com/user-attachments/assets/9413a368-22fd-441b-a835-d459aefe96e7" />



## RESULT:

Thus the program to find the sum of odd digits using for loop has been executed successfully.




# EX – 10 - Factorial of a Number Using a Function
## AIM:
To write a C program that calculates the factorial of a given number using a user-defined function.
## ALGORITHM:
1.	Start
2.	Declare the function fact().
3.	In the main() function, call the fact() function.
4.	In fact() function:
a.	Declare variables i, N, and fact (initialized to 1).
b.	Read an integer N from the user.
c.	Use a for loop from 1 to N:
i.	Multiply fact by i in each iteration.
d.	After the loop, print the factorial value.
5.	End

## PROGRAM:
```
#include <stdio.h>
void fact();

int main() {
    fact();
    
    return 0;
}
void fact() {
    int i, N;
    unsigned long long factorial = 1; 
    printf("Enter a positive integer: ");
    scanf("%d", &N);
    if (N < 0) {
        printf("Error: Factorial of a negative number doesn't exist.\n");
    } else {
        // c. Use a for loop from 1 to N
        for (i = 1; i <= N; i++) {
            // i. Multiply factorial by i
            factorial *= i;
        }
        printf("Factorial of %d is: %llu\n", N, factorial);
    }
}
```

## OUTPUT:
<img width="1280" height="566" alt="image" src="https://github.com/user-attachments/assets/b2273cad-a5e3-4519-a0ed-d50fdb053912" />

## RESULT:
The program correctly computes the factorial of a given number using a separate function and displays the result.
 
