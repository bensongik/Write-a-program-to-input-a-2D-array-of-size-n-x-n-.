# Write-a-program-to-input-a-2D-array-of-size-n-x-n-.
Display 2D arrays just entered in matrix form on the screen. Sum the elements on the main diagonal of the array
import java.util.Scanner;

public class EX4 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter n:");
        int n = sc.nextInt();
        int[][] arr = new int[n][n];
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                System.out.printf("Enter a value for arr[%d][%d]:", i, j);
                arr[i][j] = sc.nextInt();
            }
        }
        System.out.println("Display the entered array");
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                System.out.printf("%8d", arr[i][j]);
            }
            System.out.println();
        }
        int sum = 0;
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                if (i == j) {
                    sum += arr[i][j];
                }
            }
        }
        System.out.println("Sum of elements on the main diagonal of the array: " + sum);
