# Ex2 Count how many times a number appears in an array recursively.
## DATE: 22/07/2026
## AIM:
To write a Java program to Count how many times a number appears in an array recursively.

## Algorithm
1.Start

2.Read the size of the array and input all elements into the array.

3.Read the target number whose frequency you want to count.

4.Call the recursive function countOccurrences(arr, index, target) If index == arr.length, return 0 If arr[index] == target, return 1 + countOccurrences(arr, index + 1, target) Else return countOccurrences(arr, index + 1, target)

5.Display the returned count as the total number of occurrences. 

6.End

## Program:
```
/*
Program Count how many times a number appears in an array recursively.
Developed by: VINOTHKUMAR R
RegisterNumber:  212224040361
*/

import java.util.Scanner;

public class CountOccurrences {

    // Recursive function to count occurrences of a target number
    public static int countOccurrences(int[] arr, int n, int target) {
        //write your code here
        if (n == 0) {
            return 0;
        }

        // Check the last element and add 1 if it matches the target
        if (arr[n - 1] == target) {
            return 1 + countOccurrences(arr, n - 1, target);
        } else {
            return countOccurrences(arr, n - 1, target);
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Input: Size of array
        int size = scanner.nextInt();

        if (size <= 0) {
            System.out.println("Invalid array size. Must be positive.");
            return;
        }

        // Input: Array elements
        int[] arr = new int[size];
        for (int i = 0; i < size; i++) {
            arr[i] = scanner.nextInt();
        }

        // Input: Target number to count
        int target = scanner.nextInt();

        // Compute and display result
        int count = countOccurrences(arr, size, target);
        System.out.println("The number " + target + " appears " + count + " time(s) in the array.");

        scanner.close();
    }
}
```

## Output:

<img width="1027" height="611" alt="image" src="https://github.com/user-attachments/assets/8b339a84-624e-4b20-93c5-7304d201510d" />

## Result:
Thus, the Java program to Count how many times a number appears in an array recursively is implemented successfully.
