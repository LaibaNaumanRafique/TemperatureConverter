//Author: Laiba Nauman Mahmood Rafique
//date : 8 October , 2025
/*Description: This is a simple Java console application that allows the user to convert
 temperature between Fahrenheit and Celsius.
It demonstrates how to use conditional logic, switch statements,
 user input (Scanner), and basic arithmetic operations in Java.
The program asks the user to choose a conversion type (Fahrenheit →
Celsius or Celsius → Fahrenheit), then reads the
 temperature value and performs the appropriate calculation.
Finally, it displays the converted result in the correct unit.

 */

package temperatureconverter;

import java.util.Scanner;

public class TemperatureConverter {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("==== Temperature Converter ====");
        System.out.println("1. Fahrenheit to Celsius");
        System.out.println("2. Celsius to Fahrenheit");
        System.out.print("Enter your choice (1 or 2): ");
        int choice = input.nextInt();

        double temperature, result;

        switch (choice) {
            case 1:
                // Fahrenheit → Celsius
                System.out.print("Enter temperature in Fahrenheit: ");
                temperature = input.nextDouble();
                result = (temperature - 32) * 5.0 / 9.0;
                System.out.println("Temperature in Celsius: " + result + " °C");
                break;

            case 2:
                // Celsius → Fahrenheit
                System.out.print("Enter temperature in Celsius: ");
                temperature = input.nextDouble();
                result = (temperature * 9.0 / 5.0) + 32.0;
                System.out.println("Temperature in Fahrenheit: " + result + " °F");
                break;

            default:
                System.out.println("Invalid choice! Please select 1 or 2.");
        }

        input.close();
    }
}
