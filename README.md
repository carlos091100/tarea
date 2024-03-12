package com.cr.ejercicio2;

import java.io.File;
import java.io.FileWriter;
import java.io.IOException;

public class crearArchivo {

    public crearArchivo(String nombreUsuario, String contenido) throws IOException {
       
        File archivo = new File(nombreUsuario + ".txt");
        archivo.createNewFile();

       
        FileWriter escritor = new FileWriter(archivo);
        escritor.write(contenido);
        escritor.close();

        System.out.println("Archivo creado: " + archivo.getAbsolutePath());
    }
}

MAIN

package com.cr.pincipal;

import java.io.File;
import java.io.FileWriter;
import java.io.IOException;

public class Main {

    public static void main(String[] args) throws IOException {
        String nombreUsuario = "carlosrustrian";
        String contenido = "**Texto del numeral**";

  
        File archivo = new File(nombreUsuario + ".txt");
        archivo.createNewFile();


        FileWriter escritor = new FileWriter(archivo);
        escritor.write(contenido);
        escritor.close();

        System.out.println("Archivo creado: " + archivo.getAbsolutePath());
    }

}
