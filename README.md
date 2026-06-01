# Trabalho-Menu-Interativo-
## Trabalho para aula de Algoritmo e Programação - 1 Semestre. 

import javax.swing.*;
void main() {
    String menu = "    ======================\n"
            + "               Menu Principal: \n"
            + "    ======================\n"
            + " 1) Cubos dos Números de 1 a 10\n"
            + " 2) Conversor de Velocidade\n"
            + " 3) Múltiplos de 57 entre 1 e 1.000.000.\n"
            + " 4) Cálculo e Consumo de Energia\n"
            + " 0) Encerrar Programa\n\n"
            + "Escolha uma Opção: ";
    int opção = -1;

    while (opção != 0) {
        opção = Integer.parseInt(JOptionPane.showInputDialog(menu));
        switch (opção) {
            case 1:
                int numeroC = 0;
                do {
                    JOptionPane.showMessageDialog(null, "Números cubos de 1 até 10:" + "\n" +  Math.pow(numeroC, 3));
                    numeroC++;
                } while (numeroC <=10);;
                break;
            case 2:
                double velocidadeKm = Double.parseDouble(JOptionPane.showInputDialog(null,"Insira o valor em KM/h: "));
                double velocidadeMs = (velocidadeKm / 3.6);
                JOptionPane.showMessageDialog(null, "A velocidade em km/h é: \n" + velocidadeKm + "\n" + "Conversão para mt/s é: \n" + velocidadeMs);
                if (velocidadeMs >= 340) {
                    JOptionPane.showMessageDialog(null,"Você ultrapassou a VELOCIDADE DO SOM!!");
                }
                break;
            case 3:
                int multiplos = 1;
                do {
                    System.out.println("Multiplos de 57 de 1 até 1.000.00" + "\n" + multiplos % 57 * multiplos);
                    multiplos++;
                } while (multiplos <=1000000);
                break;
            case 4:
                double quantidadeHoras = Double.parseDouble(JOptionPane.showInputDialog(null, "Coloque a quantidade de horas usada no mês: "));
                double potenciaW = Double.parseDouble(JOptionPane.showInputDialog(null,"Coloque a potencia do equipamento em watts: "));

                double kwh = (quantidadeHoras * potenciaW) / 1000;
                double valor = (kwh * 0.8488);

                JOptionPane.showMessageDialog(null, "Total de Consumo: \n" + kwh +"\nValor total a ser pago: \n" + valor);
                break;
            case 0:
                JOptionPane.showMessageDialog(null, "Até logo, passar bem!!");
                break;
            default:
                JOptionPane.showMessageDialog(null,"Dado invalido");


        }
    }
}
