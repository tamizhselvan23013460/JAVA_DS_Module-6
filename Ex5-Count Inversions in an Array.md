# Ex5 Count Inversions in an Array
## DATE: 28/07/2026
## AIM:
To write a Java program  to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j

## Algorithm
1. Start the program.
2. Declare an integer array arr of size n.
3. Read the value of n (number of elements).
4. Read n elements and store them in the array arr.
5. Initialize a variable count to 0 to store the number of inversions.
6. Use two nested loops:
7. Outer loop variable i from 0 to n - 1
8. Inner loop variable j from i + 1 to n - 1
9. For each pair (i, j), if arr[i] > arr[j] and i < j, increment count by 1.
10. After all comparisons, print the value of count as the total number of inversions in the array.
11. Stop the program.

## Program:
```
/*
Program toto Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j
Developed by: VINOTHKUMAR R
RegisterNumber:  212224040361
*/

import java.util.*;

public class CountInversions {
    public static int mergeSortAndCount(int[] arr, int left, int right) 
    {
        int c=0;
        if(left<right){
            int mid=left+(right-left)/2;
            c+=mergeSortAndCount(arr,left,mid);
            c+=mergeSortAndCount(arr,mid+1,right);
            c+=mergeAndCount(arr,left,mid,right);
        }
        return c;
        
       
       
       
       
       
    }

    private static int mergeAndCount(int[] arr, int left, int mid, int right)
    {
        
        int[] la=Arrays.copyOfRange(arr,left,mid+1);
        int[] lr=Arrays.copyOfRange(arr,mid+1,right+1);
        int i=0,j=0,k=left,swap=0;
        while(i<la.length&&j<lr.length)
        {
            if(la[i]<=lr[j])
            {
                arr[k++]=la[i++];
            }else
            {
                arr[k++]=lr[j++];
                swap+=(la.length-i);
            }
        }
        while(i<la.length)
        {
            arr[k++]=la[i++];
        }
        while(j<lr.length)
        {
            arr[k++]=lr[j++];
        }
        return swap;
        
        
        
        
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) arr[i] = sc.nextInt();
        System.out.println(mergeSortAndCount(arr, 0, n - 1));
    }
}
```

## Output:

<img width="836" height="322" alt="image" src="https://github.com/user-attachments/assets/8b9da93c-21d9-4d56-be97-9bf39a23d11c" />



## Result:
Thus the Java program to to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < jis implemented successfully.
