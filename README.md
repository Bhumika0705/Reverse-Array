# Reverse-Array
Array in reverse form in java 
import java.util.Scanner;

public class ReverseArray {
    public ReverseArray() {
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the Dimensions of Array: ");
        int n = sc.nextInt();
        int m = sc.nextInt();
        int[][] arr = new int[n][m];
        System.out.println("Enter the elements of Array: ");

        int i;
        int j;
        for(i = 0; i < n; ++i) {
            for(j = 0; j < m; ++j) {
                arr[i][j] = sc.nextInt();
            }
        }

        for(i = 0; i < n; ++i) {
            j = 0;

            for(int b = m - 1; j < b; --b) {
                int temp = arr[i][j];
                arr[i][j] = arr[i][b];
                arr[i][b] = temp;
                ++j;
            }
        }

        for(i = 0; i < n; ++i) {
            for(j = 0; j < m; ++j) {
                System.out.print(arr[i][j] + " ");
            }

            System.out.println();
        }

    }
}
