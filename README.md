import java.util.Scanner;

public class Viagem {

public static void main(String[] args) {

Scanner input = new Scanner(System.in);
String placa;
double valorLitro;
double km60, km80, km100, km120, km140;

//Entrada de dados
System.out.println("Informe a placa do veículo:");
placa = input.nextLine();
System.out.println("Informe o valor do litro do combustível:");
valorLitro = input.nextDouble();
System.out.println("Informe a quantidade de quilômetros rodados a 60 km/h:");
km60 = input.nextDouble();
System.out.println("Informe a quantidade de quilômetros rodados a 80 km/h:");
km80 = input.nextDouble();
System.out.println("Informe a quantidade de quilômetros rodados a 100 km/h:");
km100 = input.nextDouble();
System.out.println("Informe a quantidade de quilômetros rodados a 120 km/h:");
km120 = input.nextDouble();
System.out.println("Informe a quantidade de quilômetros rodados a 140 km/h:");
km140 = input.nextDouble();

//Cálculo da quantidade utilizada de combustível para cada trecho
double combustivel60 = km60 / 12;
double combustivel80 = km80 / 10;
double combustivel100 = km100 / 8;
double combustivel120 = km120 / 6;
double combustivel140 = km140 / 5;

//Cálculo da quantidade total de combustível
double combustivelTotal = combustivel60 + combustivel80 + combustivel100 + combustivel120 + combustivel140;

//Cálculo da velocidade média ponderada da viagem
double velocidadeMedia = (km60 + km80 + km100 + km120 + km140) / (combustivel60 + combustivel80 + combustivel100 + combustivel120 + combustivel140);

//Cálculo do custo total da viagem
double custoTotal = combustivelTotal * valorLitro;

//Impressão dos resultados
System.out.println("Placa do veículo: " + placa);
System.out.println("Custo total da viagem: R$" + custoTotal);
System.out.println("Velocidade média ponderada da viagem: " + velocidadeMedia + " km/h");
System.out.println("Quantidade total de combustível: " + combustivelTotal + " litros");

input.close();

}

}
