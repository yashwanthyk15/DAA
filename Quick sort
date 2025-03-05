package YASHWANTHSB;
import java.util.Scanner;
import java.util.Random;
import java.util.Arrays;

public class yk252 {
    static final int MAX = 10005;
    static int[] a = new int[MAX];

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Enter Max array size: ");
        int n = input.nextInt();
        Random random = new Random();
        System.out.println("Enter the array elements: ");
        for (int i = 0; i < n; i++)
            a[i] = random.nextInt(1000);
        for (int i = 0; i < n; i++)
            System.out.print(a[i] + " ");
        long startTime = System.nanoTime();
        QuickSortAlgorithm(0, n - 1);
        long stopTime = System.nanoTime();
        long elapsedTime = stopTime - startTime;
        System.out.println("Time Complexity (ms) for n = " + n + " is : " +
                (double) elapsedTime / 1000000);
        System.out.println("Sorted Array (Quick Sort):");
        for (int i = 0; i < n; i++)
            System.out.print(a[i] + " ");
        input.close();
    }

    public static void QuickSortAlgorithm(int p, int r) {
        int i, j, temp, pivot;
        if (p < r) {
            i = p;
            j = r+1;
            pivot = a[p];
            while (true) {
                // Increment i while the element at i is less than pivot
                	i++; 
            	while (a[i] < pivot && i < r) {
                    i++;
                }
                // Decrement j while the element at j is greater than pivot
                while (a[j] > pivot) {
                    j--;
                }
                // If i < j, swap a[i] and a[j]
                if (i < j) {
                    temp = a[i];
                    a[i] = a[j];
                    a[j] = temp;
                } else {
                    break;
                }
            }
            // Swap the pivot element with the element at j
            a[p] = a[j];
            a[j] = pivot;

            // Recursively sort the two partitions
            QuickSortAlgorithm(p, j - 1);
            QuickSortAlgorithm(j + 1, r);
        }
    }
}
