// Task  # 1: Find if a number is a Harshad Number

import java.util.Scanner;

public class Main {

    // Function to calculate sum of digits
    static int digitSum(int n) {

        int sum = 0;

        while (n > 0) {
            sum += n % 10;
            n /= 10;
        }

        return sum;
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a number: ");

        int num = sc.nextInt();

        int sum = digitSum(num);

        // Check Harshad Number
        if (num % sum == 0) {

            System.out.println(num + " is a Harshad Number");

        } else {

            System.out.println(num + " is NOT a Harshad Number");
        }

        sc.close();
    }
}



// Task  # 2: Harshad Number 

class Solution {

    public int sumOfTheDigitsOfHarshadNumber(int x) {

        int original = x;
        int sum = 0;

        while (x > 0) {
            sum += x % 10;
            x /= 10;
        }

        if (original % sum == 0) {
            return sum;
        }

        return -1;
    }
}

