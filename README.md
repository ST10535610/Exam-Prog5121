import java.util.Scanner;

public class Main {

    public static <PrintProduct> void main(String[] args) {

        Scanner input = new Scanner(System.in);

        String[] productNames = {
                "Cozy Nights Monarch",
                "Restonic Barbados",
                "Sealy Phukhet"
        };

        int[][] sales = new int[3][3];

        // Enter sales information
        for (int i = 0; i < productNames.length; i++) {

            for (int j = 0; j < 3; j++) {

                System.out.print("Enter number of sales for month "
                        + (j + 1) + " for " + productNames[i]
                        + " mattress: ");

                sales[i][j] = input.nextInt();
            }
        }

        Product product = new Product(productNames, sales);

        PrintProduct report = new PrintProduct(product);

        report.PrintReport();

        input.close();
    }
}
