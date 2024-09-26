package com.mycompany.heroe;

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Heroe heroe = new Heroe("Mario", 0);  

        
        while (heroe.getVidas() > 0) {
            System.out.println("Presiona 'a' para avanzar o 's' para saltar:");
            char accion = scanner.next().charAt(0);

            if (accion == 'a') {
                heroe.avanzar();
            } else if (accion == 's') {
                heroe.saltar();
            } else {
                System.out.println("Acción no válida.");
            }
        }

        scanner.close();
    }
}
