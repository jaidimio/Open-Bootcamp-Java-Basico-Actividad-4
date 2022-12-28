# Open-Bootcamp-Java-Basico-Actividad-4
Ejercicio Actividad 4
/*  En este ejercicio tendréis que crear una clase SmartDevice. Dentro crearéis las clases hijas: SmartPhone y SmartWatch.

Agregaréis atributos tal cual tendrían esos objetos en la realidad.

Crear constructor vacío y con todos los parámetros para cada clase.

Desde una clase Main: crearéis objetos de cada una y los utilizaréis para imprimir sus valores por consola.*/

package com.Inteligentes;

public class Smart {

    public static void main(String[] args) {
        SmartPhone smartPhone = new SmartPhone(  "Samsung", "A32", 1500, 2021, true, true, true, true, true, true, true, false, 10);
        System.out.println("La información del dispositivo es:" + " " + "Marca: " + " " + smartPhone.marca + " " + "Modelo: " + " " + smartPhone.modelo + " " + "Precio: " + " " + smartPhone.price + " " + "Año: " + " " + smartPhone.year + "\n" +
                " " + "Tiene Bluetooth: " + " " + smartPhone.bluetooth + " " + "Navega con Wifi: " + " " + smartPhone.wifi + " " + "Tiene Cámara: " + "  " + smartPhone.camera + " " + "Tiene Micrófono: " + " " + smartPhone.microphone + "\n" +
                "Tiene GPS: " + " " + smartPhone.gps + " " + "Pantalla Táctil: " + " " + smartPhone.touchScreen + " " + "Le Funciona la Alarma: " + " " + smartPhone.alarm + " " + "Tiene Conectividad 5G: " + " " + smartPhone.conectividad5G + "\n"+
                "El Tiempo de la Batería es de: " + " "+ smartPhone.tiempoPila + " " + "horas");

        SmartWatch smartWatch = new SmartWatch("Samsung" , "Watch5Pro", 1000, 2020, true, false, false, true, true, true, true, true, true);
        System.out.println ("La Información del Reloj Inteligente es la Siguiente: " + " " + "La Marca es: " + smartWatch.marca + " "+ "El Modelo del Reloj es:" + " " + smartWatch.modelo + " " + "El Modelo es: " + smartWatch.modelo + " " + "El Precio es:" + " " + smartWatch.price + "\n" +
                "El año del Dispositivo es:" + " " + smartWatch.year + " " + "El Reloj se Conecta por Bluetooth:" + " " + smartWatch.bluetooth + " " + "Se Conecta al Wifi:" + " " + smartWatch.wifi + " " + "Tiene Cámara: " + " " + smartWatch.camera + "\n" +
        "El Reloj Tiene Micrófono:" + " " + smartWatch.microphone + " " + "Tiene GPS:" + " " + smartWatch.gps + " " + "El Reloj tiene Pantalla Táctil:" + " " + smartWatch.touchScreen + " " + "Se le puede configurar alarma: " + " " + smartWatch.alarm + "\n" +
         "Tiene incorporado el Control del Pulso:" + " " + smartWatch.controlPulso + " " + "Tiene Control de Tensión:" + " " + smartWatch.controlTension);
        System.out.println("Código Realizado por Jaidi González para OpenBootcamp.");

    }

    //Atributos del objeto
        public static class SmartDevice {
            public String marca;
            public String modelo;
            public double price;
            public int year;
            public boolean bluetooth;
            public boolean wifi;
            public boolean camera;
            public boolean microphone;
            public boolean gps;
            public boolean touchScreen;
            public boolean alarm;

            //Constructor Vacío
            public SmartDevice() {

            }

            public SmartDevice (String marca, String modelo, double price, int year, boolean bluetooth, boolean wifi, boolean camera, boolean microphone, boolean gps, boolean touchScreen, boolean alarm) {
                this.marca = marca;
                this.modelo = modelo;
                this.price = price;
                this.year = year;
                this.bluetooth = bluetooth;
                this.wifi = wifi;
                this.camera = camera;
                this.microphone = microphone;
                this.gps = gps;
                this.touchScreen = touchScreen;
                this.alarm = alarm;

            }
        }
    }

public class SmartPhone extends Smart.SmartDevice {

    boolean conectividad5G;
    int tiempoPila;

    public SmartPhone (String marca, String modelo, double price, int year, boolean bluetooth, boolean wifi, boolean camera, boolean microphone, boolean gps, boolean touchScreen, boolean alarm, boolean conectividad5G, int tiempoPila) {
        super (marca, modelo, price, year, bluetooth, wifi, camera, microphone, gps, touchScreen, alarm);
        this.conectividad5G = conectividad5G;
        this.tiempoPila = tiempoPila;

    }
}

public class SmartWatch extends Smart.SmartDevice {

    //Atributos
    boolean controlPulso;
    boolean controlTension;

    //Constructor Vacio
    public SmartWatch () {

    }

   public SmartWatch (String marca, String modelo, double price, int year, boolean bluetooth, boolean wifi, boolean camera, boolean microphone, boolean gps, boolean touchScreen, boolean alarm, boolean controlPulso, boolean controlTension) {
        super (marca, modelo, price, year, bluetooth, wifi, camera, microphone, gps, touchScreen, alarm);
        this.controlPulso = controlPulso;
        this.controlTension = controlTension;

    }
}

