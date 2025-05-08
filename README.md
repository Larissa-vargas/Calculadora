#include <stdio.h>
#include <stdlib.h>

int main() {
    char operacao;
    float num1, num2, resultado;

    printf("Calculadora Virtual em C\n");
    printf("Operacoes disponiveis:\n");
    printf("+ : Soma\n");
    printf("- : Subtracao\n");
    printf("* : Multiplicacao\n");
    printf("/ : Divisao\n");
    printf("q : Sair\n");

    while (1) {
        printf("\nDigite a operacao (+, -, *, /) ou 'q' para sair: ");
        scanf(" %c", &operacao);

        if (operacao == 'q') {
            printf("Saindo da calculadora...\n");
            break;
        }

        printf("Digite o primeiro numero: ");
        scanf("%f", &num1);
        printf("Digite o segundo numero: ");
        scanf("%f", &num2);

        switch (operacao) {
            case '+':
                resultado = num1 + num2;
                printf("Resultado: %.2f + %.2f = %.2f\n", num1, num2, resultado);
                break;
            case '-':
                resultado = num1 - num2;
                printf("Resultado: %.2f - %.2f = %.2f\n", num1, num2, resultado);
                break;
            case '*':
                resultado = num1 * num2;
                printf("Resultado: %.2f * %.2f = %.2f\n", num1, num2, resultado);
                break;
            case '/':
                if (num2 != 0) {
                    resultado = num1 / num2;
                    printf("Resultado: %.2f / %.2f = %.2f\n", num1, num2, resultado);
                } else {
                    printf("Erro: Divisao por zero!\n");
                }
                break;
            default:
                printf("Operacao invalida!\n");
        }
    }

    return 0;
}
