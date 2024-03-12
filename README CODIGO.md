package com.cr.examen;

import java.io.File;

public class ListarDirectorios {

    public static void listarDirectorios(String ruta) {
        File directorio = new File(ruta);

        if (directorio.isDirectory()) {
            System.out.println("Directorio encontrado: " + directorio.getAbsolutePath());

            File[] archivos = directorio.listFiles();
            if (archivos != null) {
                for (File archivo : archivos) {
                    if (archivo.isDirectory()) {
                        listarDirectorios(archivo.getAbsolutePath());
                    }
                }
            }
        } else {
            System.out.println("No es un directorio válido: " + directorio.getAbsolutePath());
        }
    }

}

main

package com.cr.test;

import com.cr.examen.ListarDirectorios;

public class Main {

    public static void main(String[] args) {
        String rutaUsuario = "C:\\Users\\rustr\\OneDrive\\Escritorio";

        ListarDirectorios.listarDirectorios(rutaUsuario);
    }

}
