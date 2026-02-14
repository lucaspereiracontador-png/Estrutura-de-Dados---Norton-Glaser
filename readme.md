# Atividades 
Este repositório contém os trabalhos da disciplina de Estrutura de Dados. ## Objetivo Implementar funções recursivas em C para estudo.

1 - Escreva uma função recursiva para calcular o valor de uma base x elevada a um expoente y:

#include <stdio.h>

int potencia(int x, int y){
    if(y == 0){
        return 1;
    }
    
    else{
        return x * potencia(x, y - 1);
    }
}

int main()
{
    int base, expoente;
    
    printf("Digite a base: ");
    scanf("%d", &base);
    
    printf("Digite o expoente: ");
    scanf("%d", &expoente);
    
    printf("%d^%d = %d\n" , base, expoente, potencia(base, expoente));
    
    return 0;
}


2 - Escrever uma função recursiva para calcular uma sequencia de Fibonacci:

A sequência de Fibonacci consiste em uma série de números, tais que, definindo seus dois primeiros números como sendo 0 e 1, os números seguintes são obtidos através da soma dos seus dois antecessores.


#include <stdio.h>

// Função recursiva para calcular o n-ésimo termo da sequência de Fibonacci
int fibonacci(int n) {
    if (n == 0) {
        return 0; // Caso base 1
    } else if (n == 1) {
        return 1; // Caso base 2
    } else {
        return fibonacci(n - 1) + fibonacci(n - 2); // Passo recursivo
    }
}

int main() {
    int termos, i;

    printf("Digite quantos termos da sequência deseja: ");
    scanf("%d", &termos);

    printf("Sequência de Fibonacci com %d termos:\n", termos);
    for (i = 0; i < termos; i++) {
        printf("%d ", fibonacci(i));
    }

    printf("\n");
    return 0;
}
