#include <stdio.h>

int main()
{
    //criacao das variaveis de pontuação, pontuação inicial e verificação caso o usuario insira uma letra.
    int pontuacao, pontuacaoIncial, verifyletter;

    printf("Digite a pontuacao inicial:");
    do{
        //scanf caso receba um int retorna 1, caso contrario retorna 0
        verifyletter = scanf("%d", &pontuacao);
        //verificacao se o caracter inserido é um int e positivo
        if(verifyletter != 1 || pontuacao < 0)
        {
            printf("Digito invalido, digite novamente:");
            //limpa o buffer da letra, necessidade de utilizar o while para ir pro ultimo caracter da linha e limpar o buffer certo
            while(getchar() != '\n');
        }
    }while(pontuacao < 0 || verifyletter != 1 );

    //armazenamento da pontuacao inicial
    pontuacaoIncial = pontuacao;

    //operacoes necessarias
    pontuacao += 50;
    printf("Pontuacao atual:%d\n", pontuacao);
    pontuacao *= 2;
    printf("Pontuacao atual:%d\n", pontuacao);
    pontuacao -=30;
    printf("Pontuacao atual:%d\n", pontuacao);
    pontuacao +=15;
    printf("Pontuacao atual:%d\n", pontuacao);
    pontuacao /= 3;
    printf("Pontuacao atual:%d\n", pontuacao);
    pontuacao += 100;
    printf("Pontuacao atual:%d\n\n", pontuacao);

    //impressão da pontuacao final e da difereça dos entre pontuacao final e inicial
    printf("Pontuacao Final:%d\n", pontuacao);
    printf("Diferenca da pontuacao inicial para final:%d", pontuacao - pontuacaoIncial);

    return 0;
}
