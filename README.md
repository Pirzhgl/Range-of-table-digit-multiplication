package equation.simple;
import java.util.Scanner;

public class Main {

        public static void main(String[] args) {
        Scanner reader = new Scanner(System.in);
        System.out.println("Введите первое число:");
        int a = reader.nextInt();
        System.out.println("Введите второе число:");
        int b = reader.nextInt();

        int[][] array = new int[3][3];
        for (int x = a; x < a + 3; x++) {
            for (int y = b; y < b + 3; y++) {
                array[x - a][y - b] = x * y;
            }
        }
        System.out.print(" \t");
        for (int i = a; i < a + 3; i++) {
            System.out.print(i + "\t");
        }
        System.out.println();
        for (int i = b; i < b + 3; i++) {
            System.out.print(i);
            for (int j = a; j < a + 3; j++) {
                System.out.print("\t" + array[j - a][i - b]);
            }
            System.out.println();
        }
    }


}
