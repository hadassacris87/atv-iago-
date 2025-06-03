# atv-iago-

//Questão 1

int main() {
    int x, y;

    printf("Insira o Numero 1: \n");
    scanf("%d", &x);

    printf("Insira o Numero 2: \n");
    scanf("%d", &y);

    printf("Soma: %d\n", x + y);

    return 0;
}


//questão 2
#include <stdio.h>

int main() {
    int numero;

    printf("Insira um número: ");
    scanf("%d", &numero);

    if (numero % 2 == 0) {
        printf("O número %d é par.\n", numero);
    } else {
        printf("O número %d é ímpar.\n", numero);
    }

    return 0;
}

//Questão 4

#include <stdio.h>

int main() {
    int a, b, c, d, e, f;
    float media;

    printf("Digite 6 números:\n");
    scanf("%d %d %d %d %d %d", &a, &b, &c, &d, &e, &f);

    media = (a + b + c + d + e + f) / 6.0;

    printf("A média é: %.2f\n", media);

    return 0;
}

//Questão 5

#include <stdio.h>

int main() {
    int ano;

    printf("Insira um ano: ");
    scanf("%d", &ano);

    if ((ano % 4 == 0 && ano % 100 != 0) || (ano % 400 == 0)) {
        printf("O ano %d é bissexto.\n", ano);
    } else {
        printf("O ano %d não é bissexto.\n", ano);
    }

    return 0;
}

//Qestão 7

#include <stdio.h>

int main() {
    int num1, num2, num3, maior;

    printf("Digite três números:\n");
    scanf("%d %d %d", &num1, &num2, &num3);

    maior = num1;
    if (num2 > maior) maior = num2;
    if (num3 > maior) maior = num3;

    printf("O maior número é: %d\n", maior);

    return 0;
}

//Questão 8

#include <stdio.h>
#include <math.h>

int main() {
    double numero, raiz;

    printf("Digite um número: ");
    scanf("%lf", &numero);

    if (numero < 0) {
        printf("Não é possível calcular a raiz quadrada de um número negativo.\n");
    } else {
        raiz = sqrt(numero);
        printf("A raiz quadrada de %.2f é %.2f\n", numero, raiz);
    }

    return 0;
}

//Questão 10

#include <stdio.h>

int main() {
    int a, b, c;

    printf("Digite os 3 lados do triângulo:\n");
    scanf("%d %d %d", &a, &b, &c);
    
    if (a + b > c && a + c > b && b + c > a) {
        if (a == b && b == c) {
            printf("Triângulo equilátero.\n");
        } else if (a == b || a == c || b == c) {
            printf("Triângulo isósceles.\n");
        } else {
            printf("Triângulo escaleno.\n");
        }
    } else {
        printf("Os valores informados não formam um triângulo.\n");
    }

    return 0;
}

//Questão 13

#include <stdio.h>

int main() {
    int n, i;
    float nota, peso, somaNotas = 0, somaPesos = 0, media;

    printf("Quantas notas você quer inserir? ");
    scanf("%d", &n);

    for (i = 1; i <= n; i++) {
        printf("Digite a nota %d: ", i);
        scanf("%f", &nota);

        printf("Digite o peso da nota %d: ", i);
        scanf("%f", &peso);

        somaNotas += nota * peso;
        somaPesos += peso;
    }

    if (somaPesos != 0) {
        media = somaNotas / somaPesos;
        printf("A média ponderada é: %.2f\n", media);
    } else {
        printf("Erro: a soma dos pesos não pode ser zero.\n");
    }

    return 0;
}

//Questão 25

#include <stdio.h>

int main() {
    float fahrenheit, celsius;

    printf("Digite a temperatura em Fahrenheit: ");
    scanf("%f", &fahrenheit);

    celsius = (5.0 / 9.0) * (fahrenheit - 32);

    printf("A temperatura em Celsius é: %.2f°C\n", celsius);

    return 0;
}

//Questão 27

#include <stdio.h>

int main() {
    float preco, novoPreco;

    printf("Digite o preço do produto: R$ ");
    scanf("%f", &preco);

    if (preco < 100) {
        novoPreco = preco * 1.10;  // aumento de 10%
    } else {
        novoPreco = preco * 1.20;  // aumento de 20%
    }

    printf("O novo preço com inflação é: R$ %.2f\n", novoPreco);

    return 0;
}

//Questao 28

#include <stdio.h>

int main() {
    float total;
    int opcao;

    printf("Total gasto: R$ ");
    scanf("%f", &total);

    printf("1-À vista\n2-Cartão\n3-2x sem juros\n4-3x com juros\nOpção: ");
    scanf("%d", &opcao);

    if (opcao == 1)
        printf("Total: R$ %.2f\n", total * 0.9);
    else if (opcao == 2)
        printf("Total: R$ %.2f\n", total);
    else if (opcao == 3)
        printf("2x de R$ %.2f\n", total / 2);
    else if (opcao == 4)
        printf("3x de R$ %.2f\n", (total * 1.1) / 3);
    else
        printf("Opção inválida.\n");

    return 0;
}


//Questão 34

#include <stdio.h>

int main() {
    char nome[50], endereco[50], telefone[20];
    int idade;

    printf("Digite seu nome: ");
    scanf("%s", nome);

    printf("Digite sua idade: ");
    scanf("%d", &idade);

    printf("Digite seu endereço: ");
    scanf("%s", endereco);

    printf("Digite seu telefone: ");
    scanf("%s", telefone);

    printf("\nSeu nome é %s, você tem %d anos, mora na rua %s e seu telefone é %s.\n", nome, idade, endereco, telefone);

    return 0;
}



