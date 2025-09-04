interface Figura {
    double calcularArea();
    double calcularPerimetro();
}

record Cuadrado(double lado) implements Figura {


    public double calcularArea() {
        return lado * lado;
    }


    public double calcularPerimetro() {
        return 4 * lado;
    }
}

record Circulo(double radio) implements Figura {


    public double calcularArea() {
        return Math.PI * radio * radio;
    }

    public double calcularPerimetro() {
        return 2 * Math.PI * radio;
    }
}

public class Main {
    public static void main(String[] args) {
        Figura f1 = new Cuadrado(4);
        Figura f2 = new Circulo(3);

        System.out.println("Área cuadrado: " + f1.calcularArea());
        System.out.println("Perímetro cuadrado: " + f1.calcularPerimetro());
        System.out.println("Área círculo: " + f2.calcularArea());
        System.out.println("Perímetro círculo: " + f2.calcularPerimetro());
    }
}
