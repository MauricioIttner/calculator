# calculator

package application;

import java.util.Locale;
import java.util.Scanner;

public class Calculator {

	public static void main(String[] args) {

		/*
		 * Essa é uma calculadora para a equação de 2ºGrau
		 */
		Locale.setDefault(Locale.US);
		Scanner sc = new Scanner(System.in);

		int a, b, c;
		double delta, x1, x2;

		a = sc.nextInt();
		b = sc.nextInt();
		c = sc.nextInt();

		delta = (b * b) + (-4 * (a * c));

		System.out.println("Delta: " + delta);

		if (delta >= 0) {

			x1 = ((- b + Math.sqrt(delta)) / (2 * a));
			x2 = ((- b - Math.sqrt(delta)) / (2 * a));

			System.out.println("x1 = " + x1);
			System.out.println("x2 = " + x2);

		} else {
			System.out.println("Delta não possui raiz!");

		}
		
		sc.close();

	}

}
