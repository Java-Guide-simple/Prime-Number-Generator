
package interviewjavaprogram;

import java.util.Scanner;

//prime number --- Numbers are divisible by only 1 and  itself.
//e.g  3,5,7,11,13,17,19.........
// Note  0,1 are not prime 

// Write a program to print prime numbers between given numbers .
public class PrimeNumber {

	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);
		System.out.print("Enter Start number ");
		int start = scan.nextInt();

		System.out.print("Enter end number ");
		int end = scan.nextInt();

		System.out.println("series of prime numbers between " + start + " and " + end);

		for (int i = start; i <= end; i++) {

			if (isPrime(i)) {
				System.out.print(i + " , ");
			}

		}

	}

	public static boolean isPrime(int number) {

		if (number <= 1) {
			return false;

		} else {
			for (int i = 2; i < number - 1; i++) {

				if (number % i == 0) {
					return false;
				}
			}

		}

		return true;

	}

}
