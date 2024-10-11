//Walter e Arthur
import java.util.Random;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Random random = new Random();
        Scanner scanner = new Scanner(System.in);

        //  controlar o loop do jogo
        boolean jogarNovamente = true;

        while (jogarNovamente) {
            // Palavras para o jogo da forca
            String[] palavras = {"sorumbatico", "liberdade", "saci", "pororoca", "flexibilidade", "explosao", "borracha", "biologo", "integridade", "youtube", "presidente", "segunda-feira", "geografia", "bem-vindo", "curso", "computador", "herdeiro", "guarda-chuva", "inss", "pneumonia", "ornitorrinco", "golfinho", "biologia ", "foca", "aposentadoria"};

            // Escolhe uma palavra aleatória
            String palavraSorteada = palavras[random.nextInt(palavras.length)];

            // Inicializa as variáveis do jogo
            int tentativas = 6;
            char[] letrasCertas = new char[palavraSorteada.length()];
            for (int i = 0; i < letrasCertas.length; i++) {
                letrasCertas[i] = '_';
            }
            String letrasErradas = "";

            // Loop do jogo
            while (tentativas > 0 && !String.valueOf(letrasCertas).equals(palavraSorteada)) {
                // Imprime a forca
                System.out.println("-------");
                System.out.println("|      |");
                if (tentativas <=5 ) {
                    System.out.println("|      O");
                } else {
                    
                }
                if (tentativas == 4) { // Tronco
                    System.out.println("|      |");
                } else {
                    System.out.println("|");
                }
                if (tentativas == 3) { // Braço esquerdo
                    System.out.println("|     \\|/");
                } else {
                    // System.out.println("|      ");
                }
                if (tentativas == 2) { // Braço direito
                    System.out.println("|     /|\\ ");
                } else {
                    System.out.println("|      ");
                }
                if (tentativas == 1) { // Perna esquerda
                    System.out.println("|      /");
                    
                    System.out.println("|     /");
                } else {
                    // System.out.println("|      ");
                    System.out.println("|      ");
                }
                System.out.println("|");
                System.out.println("-------");

                System.out.println("Palavra: " + String.valueOf(letrasCertas));
                System.out.println("Letras erradas: " + letrasErradas);
                System.out.println("Tentativas restantes: " + tentativas);
                System.out.print("Digite uma letra: ");
                char letra = scanner.next().toLowerCase().charAt(0);

                // Verifica se a letra já foi digitada
                if (letrasErradas.indexOf(letra) != -1 || String.valueOf(letrasCertas).indexOf(letra) != -1) {
                    System.out.println("Você já digitou essa letra. Tente outra.");
                } else {
                    // Verifica se a letra está na palavra
                    boolean acertou = false;
                    for (int i = 0; i < palavraSorteada.length(); i++) {
                        if (palavraSorteada.charAt(i) == letra) {
                            letrasCertas[i] = letra;
                            acertou = true;
                        }
                    }

                    // Atualiza as tentativas e letras erradas
                    if (!acertou) {
                        tentativas--;
                        letrasErradas += letra + " ";
                    }
                }

                System.out.println();
            }

            // Imprime o resultado do jogo
            if (tentativas == 0) {
                System.out.println(" pelo visto Você perdeu! tente outra vez A palavra era: " + palavraSorteada);
            } else {
                System.out.println("\u001B[33m 😮 meus Parabéns! Você acertou a palavra que eu pensei ganhou um bombom 🍬: " + palavraSorteada);
            }

            // Pergunta se o jogador quer jogar novamente
            System.out.print("Deseja jogar novamente? (s/n): ");
            String resposta = scanner.next().toLowerCase();
            if (resposta.equals("n")) {
                jogarNovamente = false;
            }
            System.out.println();
        }

        System.out.println("Obrigado por jogar!");
        scanner.close();
    }
}
