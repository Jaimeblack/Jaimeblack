



import java.util.Scanner;

public class CacaPalavras {
    private Scanner teclado;
    private String[][] palavras;
    private char[][] mapa;

    public CacaPalavras() {
        teclado = new Scanner(System.in);
        palavras = new String[5][2];
        mapa = new char[10][5];

        palavrasEntrada();
        mapaEntrada();
        mapaPesquisa();

        int opcao;
        do {
            System.out.println("_____ Menu: Caça Palavras _____");
            System.out.println("Opção 1: Imprimir Palavras");
            System.out.println("Opção 2: Imprimir Mapa");
            System.out.println("Opção 3: Respostas das Palavras");
            System.out.println("Opção 4: Sair");

            System.out.print("Escolha uma opção: ");
            opcao = teclado.nextInt();

            switch (opcao) {
                case 1:
                    palavrasImprimir();
                    break;
                case 2:
                    mapaImprimir();
                    break;
                case 3:
                    palavrasRespostas();
                    break;
                case 4:
                    System.out.println("Saindo...");
                    break;
                default:
                    System.out.println("Opção ERRADA, tente novamente!...");
            }
        } while (opcao != 4);
    }

    private void palavrasEntrada() {
        palavras[0][0] = "IFELSE";
        palavras[1][0] = "FORA";
        palavras[2][0] = "WHILE";
        palavras[3][0] = "OBJETO";
        palavras[4][0] = "VETOR";
    }

    private void palavrasImprimir() {
        for (int i = 0; i < palavras.length; i++) {
            System.out.println(palavras[i][0]);
        }
    }

    private void palavrasRespostas() {
        for (int i = 0; i < palavras.length; i++) {
            String palavra = palavras[i][0];
            int row = -1, col = -1;

            // //Realiza a busca pela palavra no mapa
             // (Você precisa implementar esta lógica com base nas regras)

            if (row == -1 || col == -1) {
                System.out.println("Palavra " + palavra + " NÃO encontrada");
            } else {
                System.out.println("Palavra " + palavra + " encontrada na posição: (" + row + ", " + col + ")");
            }
        }
    }

    private void mapaEntrada() {
        // Your provided map entries
        // ...

    }

    private void mapaImprimir() {
        // para em emprimir o mapa
        // 
    }

    private void mapaPesquisa() {
        // para procurar palavaras no mapa
    }

    public static void main(String[] args) {
        new CacaPalavras();
    }
}

