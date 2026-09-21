# Ex4 You are given a Java program that performs matrix addition. If Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension, what will be the nature (even/odd/mixed) of the resulting matrix?
## DATE:27/07/2026
## AIM:
To write a java function to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix.

## Algorithm
1. Start the program.
2. Read the dimensions of both matrices (rows and columns).
3. Check whether Matrix A and Matrix B have the same dimensions.
4. If not, display “Matrices are not of same dimension” and stop.
5. Read Matrix A and check each element:
6. If every element is odd, continue
7. If any element is even, mark A as invalid and stop further checking.
8. If both matrices are valid, compute the resultant matrix (e.g., A + B or any operation specified).
9. Determine the nature of the resultant matrix:
10. If all elements are odd, print “Resultant matrix is an Odd Matrix”.
11. If all elements are even, print “Resultant matrix is an Even Matrix”.
12. Display the Resultant Matrix.
13. Stop the program.

## Program:
```
/*
Program to ind the nature of resultant matrrix.
Developed by: VINOTHKUMAR R
RegisterNumber:  212224040361
*/\
import java.util.Scanner;

public class MatrixAddition {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int rows = sc.nextInt();
        int cols = sc.nextInt();

        int[][] A = new int[rows][cols];
        int[][] B = new int[rows][cols];
        int[][] result = new int[rows][cols];

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                A[i][j] = sc.nextInt();
            }
        }
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                B[i][j] = sc.nextInt();
            }
        }
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                result[i][j] = A[i][j] + B[i][j];
            }
        }
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                System.out.print(result[i][j] + " ");
            }
            System.out.println();
        }

       
    }
}

```

## Output:

<img width="422" height="624" alt="513775109-34782319-f865-4fe8-a281-f3aed6852160" src="https://github.com/user-attachments/assets/bb76cdae-96d6-411b-9858-d37832ff0405" />


## Result:
Thus, the java program to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix is implemented successfully.
