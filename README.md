  task 8

1.Write a Java program that declares four integer variables: a, b, c, and d. Then, write an if statement that checks whether the sum of a and b is greater than the sum of c and d. If the condition is true, the program should output a message indicating that the sum of a and b is greater than the sum of c and d.

import java.util.Scanner;
public class CompareSumsWithScanner {
    public static void main(String[] args) {
 Scanner scanner = new Scanner(System.in);
 System.out.println("Enter the value of a:");
        int a = scanner.nextInt();
 System.out.println("Enter the value of b:");
int b = scanner.nextInt();

        System.out.println("Enter the value of c:");
        int c = scanner.nextInt();

        System.out.println("Enter the value of d:");
        int d = scanner.nextInt();

         
        if (a + b > c + d) {
     System.out.println("The sum of a and b is greater than the sum of c and d.");
        } else {
            System.out.println("The sum of a and b is not greater than the sum of c and d.");
        }
        scanner.close();
    }
}

2. Have a variable store an integer. Create an if statement to find out if it's an even number. Hint: Use operator %.
Ans:
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
 Scanner scanner = new Scanner(System.in);
   System.out.print("Enter an integer: ");
   int number = scanner.nextInt();
   if (number % 2 == 0) {
            System.out.println(number + " is an even number.");
        } else {
            System.out.println(number + " is an odd number.");
        }
        scanner.close();
    }
}
3. Write a program to print the characters from A to Z.

import java.util.Scanner;
public class PrintAlphabets {
    public static void main(String[] args) {
     Scanner scanner = new Scanner(System.in);
      System.out.print("Enter a number of characters to print (A to Z): ");
       int numberOfCharacters = scanner.nextInt();
          scanner.close();
       for (char c = 'A'; c <= ('A' + numberOfCharacters - 1); c++) 
{
            System.out.print(c + " ");
        }
    }
}

4. Write a java program to get 2 numbers from the user and swap their values without any loss of data. You can make use of additional variable for swapping. Print the corresponding swapped values of the two numbers as output in the console.
Ans: import java.util.Scanner;
public class SwapNumbers{
    public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);
       System.out.print("Enter the first number: ");
        int firstNumber = scanner.nextInt();
        System.out.print("Enter the second number: ");
        int secondNumber = scanner.nextInt();
         System.out.println("Before swapping:");
        System.out.println("First number: " + firstNumber);
        System.out.println("Second number: " + secondNumber);
         int temp = firstNumber;
        firstNumber = secondNumber;
        secondNumber = temp;
       System.out.println("\nAfter swapping:");
        System.out.println("First number: " + firstNumber);
        System.out.println("Second number: " + secondNumber);
        scanner.close();
    }
}


5. Write a program to check if a number is prime or not.
Ans:
import java.util.Scanner;

public class PrimeNumberChecker {
    public static void main(String[] args) {
        // Create a Scanner object to read input
        Scanner scanner = new Scanner(System.in);

        // Prompt the user to enter a number
        System.out.print("Enter a number: ");
        int number = scanner.nextInt();

        // Close the scanner
        scanner.close();

        // Check if the number is prime
        boolean isPrime = checkPrime(number);

        // Display the result
        if (isPrime) {
            System.out.println(number + " is a prime number.");
        } else {
            System.out.println(number + " is not a prime number.");
        }
    }

    // Method to check if a number is prime
    public static boolean checkPrime(int num) {
        // 0 and 1 are not prime numbers
        if (num <= 1) {
            return false;
        }

        // Check for divisibility from 2 to the square root of the number
        for (int i = 2; i <= Math.sqrt(num); i++) {
            if (num % i == 0) {
                return false;
            }
        }
        return true;
    }
}


6. Write a program to print the factorial of a given number. For Ex: 5!-120
Ans : 
import java.util.Scanner;

public class FactorialCalculator {
    public static void main(String[] args) {
        // Create a Scanner object to read input
        Scanner scanner = new Scanner(System.in);

        // Prompt the user to enter a number
        System.out.print("Enter a number to calculate its factorial: ");
        int number = scanner.nextInt();

        // Close the scanner
        scanner.close();

        // Calculate the factorial of the number
        int factorial = calculateFactorial(number);

        // Display the factorial
        System.out.println(number + "! = " + factorial);
    }

    // Method to calculate the factorial of a number
    public static int calculateFactorial(int n) {
        if (n == 0 || n == 1) {
            return 1;
        } else {
            return n * calculateFactorial(n - 1);
        }
    }
}

7. Write a program to print the length of the given string. String msg="Guvi Geek"
Ans: import java.util.Scanner;

public class StringLength {
    public static void main(String[] args) {
        // Create a Scanner object to read input from the user
        Scanner scanner = new Scanner(System.in);

        // Prompt the user to enter a string
        System.out.print("Enter a string: ");
        
        // Read the input string from the user
        String msg = scanner.nextLine();
        
        // Close the scanner to prevent resource leak
        scanner.close();

        // Calculate the length of the string
        int length = msg.length();

        // Print the length of the string
        System.out.println("Length of the string is: " + length);
    }
}

8. Write a program To print "Welcome to Guvi" 10 times.
Ans :
public class WelcomeToGuvi {
    public static void main(String[] args) {
        // Define the string to be printed
        String message = "Welcome to Guvi";

        // Print the message 10 times using a loop
        for (int i = 0; i < 10; i++) {
            System.out.println(message);
        }
    }
}

9. Write a program to check whether the person is a senior citizen or not.
Ans:
import java.util.Scanner;

public class SeniorCitizenChecker {
    public static void main(String[] args) {
        // Create a Scanner object to read input from the user
        Scanner scanner = new Scanner(System.in);

        // Prompt the user to enter their age
        System.out.print("Enter your age: ");

        // Read the age input from the user
        int age = scanner.nextInt();

        // Close the scanner to prevent resource leak
        scanner.close();

        // Define the age threshold for senior citizenship
        int seniorCitizenAge = 60;

        // Check if the person is a senior citizen
        if (age >= seniorCitizenAge) {
            System.out.println("You are a senior citizen.");
        } else {
            System.out.println("You are not a senior citizen.");
        }
    }
}
10. I). Write a program to Count Number of Digits in an Integer.
Ans :    import java.util.Scanner;

public class CountDigits {
    public static void main(String[] args) {
        // Create a Scanner object to read input from the user
        Scanner scanner = new Scanner(System.in);

        // Prompt the user to enter an integer
        System.out.print("Enter an integer: ");

        // Read the integer input from the user
        int number = scanner.nextInt();

        // Close the scanner to prevent resource leak
        scanner.close();

        // Convert the integer to a string to count its digits
        String numberString = String.valueOf(number);

        // Count the number of digits in the integer
        int numberOfDigits = numberString.length();

        // Print the number of digits in the integer
        System.out.println("Number of digits in the integer: " + numberOfDigits);
    }
}
