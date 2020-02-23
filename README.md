# Largest-in-array-Java_interview_practice
Java program to find largest number in array

package largestinarray;

import java.util.Scanner;

/**
 *
 * @author Dinesh Nanda
 */
public class Largest_In_Array {

    public static void main(String[] args) {
        
        Scanner s = new Scanner(System.in);
        System.out.println("Enter the size of an array:");
        int array_size = s.nextInt();

        int arr[];

        arr = new int[array_size];

        System.out.println("Enter the elements of an array: ");

        for (int i = 0; i < array_size; i++) {
            arr[i] = s.nextInt();
        }
        System.out.print("Your entered array is: ");
        for (int i = 0; i < array_size; i++) {
            System.out.print(arr[i]+" ");
        }
        System.out.println();
        
        int largest = arr[0];

        for (int i = 0; i < array_size - 1; i++) {
            
            if(largest < arr[i+1]){
                largest = arr[i+1];
            }
        }
        System.out.println("Largest number in array is: "+ largest);
        
    }
}
