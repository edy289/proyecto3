# proyecto3

\\creamos usuario para el sistema

import java.util.*;
import java.io.*;

class Usuario {
private int id;
private String nombre;
private String apellidos;
private String contraseña;
    
public Usuario(int id, String nombre, String apellidos, String contraseña) {
this.id = id;       
this.nombre = nombre;
this.apellidos = apellidos;      
this.contraseña = contraseña;
    }   
    }
    


package com.mycompany.usuario;



import java.util.Date;

class Caja {
    private int correlativo;
    
   
private Date fechaIngreso;
    public Caja(int correlativo, Date fechaIngreso) {       
this.correlativo = correlativo;
this.fechaIngreso = fechaIngreso;
    }
    }
    
    
    
    
package com.mycompany.usuario;

/**
 *
 * @author leove
 */
public class Cliente {

    
   
private int cui;
    
   
private String nombre;
    
   
private String apellidos;
    
   
private String telefono;
    
   
private String direccion;
    
    
    
   

    
public Cliente(int cui, String nombre, String apellidos, String telefono, String direccion) {
        
       
this.cui = cui;
        
       
this.nombre = nombre;
        
       
this.apellidos = apellidos;
        this.telefono = telefono;
        
       
this.direccion = direccion;
    }
    
    
    }
    


package com.mycompany.usuario;

/**
 *
 * @author leove
 */
public class Repartidor {
       
private int cui;
private String nombre; 
private String apellidos; 
private String licencia;  
private String telefono;
    
    
public Repartidor(int cui, String nombre, String apellidos, String licencia, String telefono) {
        
       
this.cui = cui;
        this.nombre = nombre;      
this.apellidos = apellidos;
        this.licencia = licencia;     
this.telefono = telefono;
    }
    
    
    }
    
    
    package com.mycompany.usuario;

/**
 *
 * @author leove
 */
public class Vehículo {
   

class Vehiculo {
private String placa; 
private String marca; 
private String modelo;  
private String color;  
private int año;
    
    
    
   

    
public Vehiculo(String placa, String marca, String modelo, String color, int año) {
        
       
this.placa = placa;     
this.marca = marca;     
this.modelo = modelo;      
this.color = color;      
this.año = año;
    }
    
    
    }

}


package com.mycompany.usuario;

/**
 *
 * @author leove
 */
public class Vehículo {
   

class Vehiculo {
private String placa; 
private String marca; 
private String modelo;  
private String color;  
private int año;
    
    
    
   

    
public Vehiculo(String placa, String marca, String modelo, String color, int año) {
        
       
this.placa = placa;     
this.marca = marca;     
this.modelo = modelo;      
this.color = color;      
this.año = año;
    }
    
    
    }

}



package com.mycompany.usuario;



import java.io.BufferedReader;
import java.io.FileNotFoundException;
import java.io.FileReader;
import java.io.IOException;
import java.util.Stack;

public class SistemaEnlatados {
    private LinkedList<Usuario> usuarios;
    private Stack<Caja> almacen;
    private AVLTree<Cliente> clientes;
    private Queue<Repartidor> repartidores;
    private Queue<Vehiculo> vehiculos;
    private LinkedList<Pedido> pedidos;
    
    public SistemaEnlatados() {
        usuarios = new LinkedList<>();
        almacen = new Stack<>();
        clientes = new AVLTree<>();
        repartidores = new LinkedList<>();
        vehiculos = new LinkedList<>();
        pedidos = new LinkedList<>();
    }
    
    
    
    public void generarReportes() {
        generarReporteUsuarios();
        generarReporteAlmacen();
        generarReporteClientes();
        generarReporteRepartidores();
        generarReporteVehiculos();
        generarReportePedidos();
    }
    
    private void generarReporteUsuarios() {   
    }
    private void generarReporteAlmacen() { 
    }
    private void generarReporteClientes() {
    }
    private void generarReporteRepartidores() { 
    }
    private void generarReporteVehiculos() {
    }
    private void generarReportePedidos() {  
    }
    
    public static void main(String[] args) throws FileNotFoundException, IOException {
        // Crear una instancia del sistema
        SistemaEnlatados sistema = new SistemaEnlatados();
        
      
        // Cargar usuarios desde archivo
        try {
            FileReader fileReader = new FileReader("usuarios.csv");
            BufferedReader bufferedReader = new BufferedReader(fileReader);
            
            String line;
            while ((line = bufferedReader.readLine()) != null) {
                String[] data = line.split(";");
                int id = Integer.parseInt(data[0]);
                String nombre = data[1];
                String apellidos = data[2];
                String contraseña = data[3];
                
                Usuario usuario = new Usuario(id, nombre, apellidos, contraseña);
                sistema.usuarios.add(usuario);
        }
        }
    }
            
           
