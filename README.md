# courselevel
import java.util.Scanner;

public class CGPACalculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of subjects: ");
        int n = sc.nextInt();

        double totalCredits = 0;
        double totalWeightedPoints = 0;

        for (int i = 1; i <= n; i++) {
            System.out.println("Subject " + i + ":");

            System.out.print("  Enter rating (e.g. 10, 9, etc.): ");
            double rating = sc.nextDouble();

            System.out.print("  Enter credit (e.g. 4, 3, etc.): ");
            double credit = sc.nextDouble();

            totalWeightedPoints += rating * credit;
            totalCredits += credit;
        }

        double cgpa = totalWeightedPoints / totalCredits;
        System.out.printf("\nYour CGPA is: %.2f\n", cgpa);

        sc.close();
    }
}
