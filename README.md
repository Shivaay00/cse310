# cse310
scientific Calculator made by java
import java.util.Scanner;
import java.lang.Math;

public class ScientificCalculator {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        double num1, num2;
        String operation;

        System.out.print("Enter first number: ");
        num1 = input.nextDouble();

        System.out.print("Enter second number: ");
        num2 = input.nextDouble();

        System.out.println("Select an operation (+, -, *, /, sin, cos, tan, log, sqrt): ");
        operation = input.next();

        switch (operation) {
            case "+":
                System.out.println(num1 + " + " + num2 + " = " + (num1 + num2));
                break;

            case "-":
                System.out.println(num1 + " - " + num2 + " = " + (num1 - num2));
                break;

            case "*":
                System.out.println(num1 + " * " + num2 + " = " + (num1 * num2));
                break;

            case "/":
                if (num2 == 0) {
                    System.out.println("Cannot divide by zero");
                } else {
                    System.out.println(num1 + " / " + num2 + " = " + (num1 / num2));
                }
                break;

            case "sin":
                System.out.println("sin(" + num1 + ") = " + Math.sin(num1));
                break;

            case "cos":
                System.out.println("cos(" + num1 + ") = " + Math.cos(num1));
                break;

            case "tan":
                System.out.println("tan(" + num1 + ") = " + Math.tan(num1));
                break;

            case "log":
                System.out.println("log(" + num1 + ") = " + Math.log10(num1));
                break;

            case "sqrt":
                System.out.println("sqrt(" + num1 + ") = " + Math.sqrt(num1));
                break;

            default:
                System.out.println("Invalid operation");
                break;
        }
    }
}
