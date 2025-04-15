# AulaPOO
Trabalhos e exercicios de POO


-------------------------------------------------------------------------------

package jogo;

public abstract class Jogo {
    protected String nome;

    public Jogo(String nome) {
        this.nome = nome;
    }

    public String getNome() {
        return nome;
    }

    public abstract void iniciar();
}


-------------------------------------------------------------------------------


package jogo;

public class Palavra {
    private String texto;

    public Palavra(String texto) {
        this.texto = texto.toUpperCase();
    }

    public String getTexto() {
        return texto;
    }
}


-------------------------------------------------------------------------------

package jogo;

import java.util.Scanner;

public class CacaPalavras extends Jogo {

    public CacaPalavras() {
        super("Caça-Palavras");
    }

    @Override
    public void iniciar() {
        System.out.println("=== Jogo de Caça-Palavras ===");
        // Aqui virá a lógica de montar a matriz e buscar palavras
        Scanner scanner = new Scanner(System.in);
        System.out.println("Funcionalidade em desenvolvimento...");
    }
}


-------------------------------------------------------------------------------

package jogo;

import java.util.Scanner;

public class JogoDescoberta extends Jogo {

    public JogoDescoberta() {
        super("Jogo da Descoberta");
    }

    @Override
    public void iniciar() {
        System.out.println("=== Jogo da Descoberta ===");
        // Aqui virá a lógica do jogo da descoberta
        Scanner scanner = new Scanner(System.in);
        System.out.println("Funcionalidade em desenvolvimento...");
    }
}


-------------------------------------------------------------------------------

package jogo;

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Jogo jogoSelecionado;

        System.out.println("Escolha um jogo:");
        System.out.println("1 - Caça-Palavras");
        System.out.println("2 - Jogo da Descoberta");
        int opcao = scanner.nextInt();

        if (opcao == 1) {
            jogoSelecionado = new CacaPalavras();
        } else if (opcao == 2) {
            jogoSelecionado = new JogoDescoberta();
        } else {
            System.out.println("Opção inválida.");
            return;
        }

        jogoSelecionado.iniciar();
    }
}

-------------------------------------------------------------------------------

