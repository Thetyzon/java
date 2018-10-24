package com.company;
import java.sql.SQLOutput;
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        float distancia = 0;
        float velocidadp = 0;
        float tiempo = 0;
        float velocidadmedia = 0;

        Scanner teclado = new Scanner(System.in);

       while (true) {
           distancia = teclado.nextInt();
           velocidadp = teclado.nextInt();
           tiempo = teclado.nextInt();

           if (distancia == 0 | velocidadp == 0 | tiempo == 0) {
           System.exit(1);
           }

           else if (distancia > 0 | velocidadp > 0 | tiempo > 0) {
               distancia = distancia / 1000;
               tiempo = tiempo / 3600;
               velocidadmedia = distancia / tiempo;
           }
           else if (distancia < 0 | velocidadp < 0 | tiempo < 0) {
               System.out.println("ERROR");
           }
               if (velocidadmedia <= velocidadp) {
                   System.out.println("OK");
               }
               else if (velocidadmedia >= velocidadp){
                   System.out.println("MULTA");
               }

       }
    }
}
