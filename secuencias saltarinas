package secuenciassaltarinas;

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.HashSet;
import java.util.Set;
import java.util.StringTokenizer;

public class SecuenciasSaltarinas {

    public static final String SI = "Es Secuencia Saltarira"; // El final indica que ya no puede ser cambiado una vez declarado
    public static final String NO = "No es Secuencia Saltarina"; // El final indica que ya no puede ser cambiado una vez declarado 

    public static void main(String[] args) throws IOException {
        final BufferedReader bf = new BufferedReader(new InputStreamReader(System.in)); // El final indica que ya no puede ser cambiado una vez declarado
        String linea;

        while ((linea = bf.readLine()) != null) {
            linea = linea.trim();

            if (!linea.equals("")) { // equals se utiliza para comparar dos objetos
                StringTokenizer token = new StringTokenizer(linea); // Se usa para separar los Strings
                int length = Integer.parseInt(token.nextToken());
                int[] secuencia = new int[length];
                int a = 0; // 'a' se va a igualar a 0
                while (token.hasMoreTokens()) {
                    int valor = Integer.parseInt(token.nextToken());
                    if (a < length) { // Si a es menor a longitud
                        secuencia[a++] = valor; // Entonces a++
                    }
                }

                System.out.println(resolver(secuencia, length));
            }
        }
    }

    public static String resolver(int[] sequencia, int length) {
        if (length == 1) { // Si longitud es igual a 1
            return SI;
        }

        Set< Integer> diferencia = new HashSet< Integer>(); // HashSet construye un nuevo conjunto
        for (int i = 0; i < length - 1; i++) {
            int diff = Math.abs(sequencia[i + 1] - sequencia[i]);
            if (diff <= length - 1 && diff > 0) {
                diferencia.add(diff);
            }
        }

        return (diferencia.size() == length - 1) ? SI : NO;
    }
}
