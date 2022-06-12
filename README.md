# O intuito desse GitHub, é servi de portfólio de exemplos de códigos e assuntos ligados a estudos e obtenção de prática
# e experiência dentro da programação e desenvolvimento de software, atualmente sou estudante de engenharia de Software # e da Segurança da Informação assim como estou construindo conhecimentos como desenvolvedora full stack
# possuo outro GitHub que pretendo focar em projetos pessoais com objetivos sócias, ecológicos, políticos e econômicos
# Esses exercício foram os primeiros que pesquisei na linguagem Java, e posteriomente em outras linguagens e tecnologias # que estudei recentemente, esses exercícios foram os primeiros em aprofundamento de seus significados sobre lógicas computacional.

# Nota pessoal:

# As dificuldades e diversidades do dia a dia, me transformaram, assim como a entrada da tecnologia em minha vida 
# e a busca por conhecimentos
# e oportunidades, tem moldado quem sou profissionalmente e como pessoa, moldando como percebo o mundo e suas lições 
# a modificação de hábitos, de profissão, de projetos e pensamentos vem construindo uma versão melhor do que tinha sido
# até aqui
# 
# Eu não sou o que me acontece, eu sou o que escolho me tornar. " Carl Jung'
#

//Wello World Java e implementação de uma fila com 100 elementos


public class HelloWorld {
 public static void main (String args[]) {
 System.out.println("Hello World!");
 }
}

import javax.swing.*;

class Fila{
    int inicio;
    int fim;
    int tamanho;
    int qtdeElementos;
    int f[];

    public Fila(){
        inicio = fim = -1;
        tamanho = 100;
        f = new int[tamanho];
        qtdeElementos = 0;
    }

    public boolean estaVazia(){
        if (qtdeElementos == 0){
            return true;
        }
        return false;
    }

    public boolean estaCheia(){
        if (qtdeElementos == tamanho - 1){
            return true;
        }
        return false;
    }

    public void adicionar(int e){
        if (! estaCheia()){
            if (inicio == -1){
                inicio = 0;
            }
            fim++;
            f[fim] = e;
            qtdeElementos++;
        }
    }

    public void remover(){
        if (! estaVazia() ){
            inicio++;
            qtdeElementos--;
        }
    }

    public void mostrar(){
        String elementos = "";
            for (int i = inicio; i<=fim; i++) {
                elementos += f[i]+ " - ";
            }
            JOptionPane.showMessageDialog(null, elementos);
    }
}

public class FilaAplicacao {
    public static void main(String[] args) {
        Fila f = new Fila();        
        f.adicionar(10);
        f.adicionar(12);
        f.adicionar(30);
        f.mostrar();
        f.remover();
        f.mostrar();
    }
}
