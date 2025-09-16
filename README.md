import java.util.Scanner;
public class TemperatureConveter {

    public static double celsiusToFahrenheit(double celsius) {
        return (celsius * 9 / 5) + 32;
    }

    public static double celsiusToKelvin(double celsius) {
        return celsius + 273.15;
    }

    public static double fahrenheitToCelsius(double fahrenheit) {
        return (fahrenheit - 32) * 5 / 9;
    }

    public static double fahrenheitToKelvin(double fahrenheit) {
        return (fahrenheit - 32) * 5 / 9 + 273.15;
    }

    public static double kelvinToCelsius(double kelvin) {
        return kelvin - 273.15;
    }

    public static double kelvinToFahrenheit(double kelvin) {
        return (kelvin - 273.15) * 9 / 5 + 32;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Temperature Converter");
        System.out.println("Available scales: Celsius (C), Fahrenheit (F), Kelvin (K)");

        System.out.print("Enter the temperature value: ");
        double value = scanner.nextDouble();

        System.out.print("Enter the input scale (C/F/K): ");
        char scale = scanner.next().toUpperCase().charAt(0);

        switch (scale) {
            case 'C':
                System.out.printf("Celsius: %.2f °C%n", value);
                System.out.printf("Fahrenheit: %.2f °F%n", celsiusToFahrenheit(value));
                System.out.printf("Kelvin: %.2f K%n", celsiusToKelvin(value));
                break;

            case 'F':
                System.out.printf("Fahrenheit: %.2f °F%n", value);
                System.out.printf("Celsius: %.2f °C%n", fahrenheitToCelsius(value));
                System.out.printf("Kelvin: %.2f K%n", fahrenheitToKelvin(value));
                break;

            case 'K':
                System.out.printf("Kelvin: %.2f K%n", value);
                System.out.printf("Celsius: %.2f °C%n", kelvinToCelsius(value));
                System.out.printf("Fahrenheit: %.2f °F%n", kelvinToFahrenheit(value));
                break;

            default:
                System.out.println("Invalid input scale. Please enter C, F, or K.");
        }

        scanner.close();
    }
}# TemperatureConvter
