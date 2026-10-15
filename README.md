import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Ingresa un numero entero:");
        int numero = scanner.nextInt();
        if (numero > 0) {
            System.out.println("El numero," + numero + ",es POSITIVO");
        } else if (numero < 0) {
            System.out.println("El numero es," + numero + "es NEGATIVO");
        } else {
            System.out.println("El numero es CERO");
        }
        System.out.println("------------------------");

        System.out.print("Ingresa tu edad: ");
        int edad = scanner.nextInt();

        // Cadena de if - else if para determinar la categoría según el rango
        if (edad >= 0 && edad <= 12) {
            System.out.println("Categoría: Niño");
        } else if (edad >= 13 && edad <= 17) {
            System.out.println("Categoría: Adolescente");
        } else if (edad >= 18 && edad <= 64) {
            System.out.println("Categoría: Adulto");
        } else if (edad >= 65) {
            System.out.println("Categoría: Adulto mayor");
        } else {
            System.out.println("Por favor, ingresa una edad válida (número positivo).");
        }
        System.out.println("-----------------------");


        System.out.print("Ingresa el primer número entero: ");
        int num1 = scanner.nextInt();

        System.out.print("Ingresa el segundo número entero: ");
        int num2 = scanner.nextInt();

        System.out.print("Ingresa la operación (+, -, *, /): ");
        String operacion = scanner.next();

        // Estructura switch mejorada
        switch (operacion) {
            case "+" -> System.out.println("Resultado: " + num1 + " + " + num2 + " = " + (num1 + num2));
            case "-" -> System.out.println("Resultado: " + num1 + " - " + num2 + " = " + (num1 - num2));
            case "*" -> System.out.println("Resultado: " + num1 + " * " + num2 + " = " + (num1 * num2));
            case "/" -> {
                // Validación para evitar la división entre cero
                if (num2 != 0) {
                    System.out.println("Resultado: " + num1 + " / " + num2 + " = " + ((double) num1 / num2));
                } else {
                    System.out.println("Error: No se puede dividir entre cero.");
                }
            }
            default -> System.out.println("Error: Operador inválido.");
        }
        System.out.println("---------------------------------------");
        System.out.println("Cuenta regresiva");
        for (int i = 10; i >= 1; i--) {
            System.out.println(i);
        }
        System.out.println("---------------------------------");
        System.out.println("Encontrar el numero mayor:");
        int[] numerosDesordenados = {25, 8, 92, 43, 5, 67};
        int mayor = numerosDesordenados[0];
        for (int numero2 : numerosDesordenados) {
            if (numero2 > mayor) {
                mayor = numero2;
            }
        }
        System.out.println("El numero mayor del arreglo es:" + mayor);
        System.out.println("-------------------------------------------------");
        System.out.println("Numeros divisibles entre 3");
        for (int i = 1; i <= 20; i++) {
            if (i % 3 == 0) {
                System.out.println(i);
            }
            System.out.println("----------------------------------------");
            System.out.println("Registro de notas");
            int calificacion = 0;
            int aprobados = 0;
            int reprobados = 0;

            while (calificacion != -1) {
                System.out.println("Ingresa la calificacion del alumno (0 a 100) o -1 para terminar:");
                calificacion = scanner.nextInt();

                if (calificacion >= 60 && calificacion <= 100) {
                    aprobados++;
                } else if (calificacion >= 0 && calificacion < 60) {
                    reprobados++;
                } else if (calificacion != -1) {
                    System.out.println("Calificación inválida. Ingresa un número entre 0 y 100.");

                }
            }
            System.out.println("\n--- Resultados Finales ---");
            System.out.println("Total de alumnos aprobados (>= 60): " + aprobados);
            System.out.println("Total de alumnos reprobados (< 60): " + reprobados);

        }

    }
}