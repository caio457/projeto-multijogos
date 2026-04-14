# projeto-multijogos



#include <stdio.h>
#include <stdlib.h>
#include <time.h>
#include <locale.h>
 

 
 // jogo 1 perguntas e repostas 
void PerguntasErespostas() {

	
	
char r1 , r2 , r3 , r4 , r5;
char escolha ;
setlocale(LC_ALL, "Portuguese");

do{		

	
	
printf ("Qual destes NÃO é um sistema operacional?\n");
printf("A-linux\n");
printf("B-windows\n");
printf("C-macOS\n");
printf("D-chrome\n");        
printf("responda: ");                                   //pergunta 1
scanf(" %c", &r1);
if(r1 == 'D'||r1 == 'd' )
{
	printf ("resposta correta ");
}
else 
printf ("resposta incorreta\n");
printf ("       \n");                                                                                            
printf ("       \n");
printf ("       \n");





printf ("O que significa a sigla CPU? ?\n");
printf("A-Central Process Unit\n");
printf("B- Computer Personal Unit\n");
printf("C-Central Processing Unit\n");
printf("D-Control Processing User\n");                             //pergunta 2
printf("responda: ");
scanf(" %c", &r2);
if(r2 == 'C'||r2 == 'c' )
{
	printf ("resposta correta ");
}
else 
printf ("resposta incorreta");





printf ("       \n");
printf ("       \n");
printf ("       \n");

printf ("Em linguagem C, qual símbolo é usado para “e lógico” (AND ?\n");
printf("A-&&\n");
printf("B- ||\n");
printf("C-%%\n");
printf("D-!!\n");                                    // pergunta 3
printf("responda: ");
scanf(" %c", &r3);
if(r3 == 'A'||r3 == 'a' )
{
	printf ("resposta correta ");
}
else 
printf ("resposta incorreta");




printf ("       \n");
printf ("       \n");
printf ("       \n");

printf (" Qual linguagem é mais usada para desenvolvimento web no lado do cliente (front-end)?\n");
printf("A-python\n");
printf("B-javascript\n");
printf("C-java\n");                                    // pergunta 4
printf("D-C\n");
printf("responda: ");
scanf(" %c", &r4);
if(r4 == 'B'||r4 == 'b' )
{
	printf ("resposta correta ");
}
else 
printf ("resposta incorreta");



printf ("       \n");
printf ("       \n");
printf ("       \n");



printf (" Qual é o resto dessa expressão 5/2 ?\n");
printf("A-0\n");
printf("B-3\n");
printf("C-1\n");                                    // pergunta 5
printf("D-2\n");
printf("responda: ");
scanf(" %c", &r5);
if(r5 == 'C'||r5 == 'c' )
{
	printf ("resposta correta ");
}
else 
printf ("resposta incorreta\n");




printf ("quer continuar ? ");
printf("s - sim \t n - nao\n");
printf("Escolha: ");
scanf(" %c", &escolha);
system ("cls");

}while(escolha =='s');

}

// jogo 2 cobra na caixa 
void cobraNaCaixa() {
    
	
	char escolha2 ;
	
do{	
	

	
	
char nomes[7][50] = {"jogador 1","jogador 2","jogador 3", "jogador 4", "jogador 5", "jogador 6", "jogador 7"};
    int sorteio;
   

    srand(time(NULL));

    sorteio = rand() % 5;

    printf("Nome sorteado: %s\n", nomes[sorteio]);
    
    
    
    
  srand(time(NULL)); 

    sorteio = rand() % 5;
    int caixas[5] = {0, 0, 0, 0, 0}; // 0 = vazia
    int botao, cobra;
    int escolha , jogador;
    int abertas[5] = {0, 0, 0, 0, 0}; // controla caixas já abertas

   srand(time(NULL)); // significa e o gerador de numeros aleatorios 

    // sorteia posição do botão
    botao = rand() % 5; // vai sortear ate 5

    // sorteia posição da cobra (diferente do botão)       // parte com chat gpt 
    do {
        cobra = rand() % 5;
    } while(cobra == botao);

    caixas[botao] = 1; // botão
    caixas[cobra] = -1; // cobra

    printf("   COBRA NA CAIXA  \n");

    while(1) {
        printf("\n %s, escolha uma caixa (1 a 5): ", nomes[sorteio]);
        scanf("%d", &escolha);

        escolha--; // ajustar para índice 0 a 4

        // validação
        if(escolha < 0 || escolha > 4) {
            printf("Escolha invalida!\n");
            continue;
        }

        if(abertas[escolha] == 1) {
            printf("Essa caixa ja foi aberta! Escolha outra.\n");
            continue;
        }

        abertas[escolha] = 1;

        // verifica conteúdo
        if(caixas[escolha] == 1) {
            printf(" BOTAO! Jogador %2 venceu!\n", nomes[sorteio]);
            break;
        } 
        else if(caixas[escolha] == -1) {
            printf(" COBRA! Jogador %2 perdeu!\n", nomes[sorteio]);
            break;
        } 
        else {
            printf("Caixa vazia...\n");
        }

        // troca jogador
        if(jogador == 1)
            jogador = 2;
        else
            jogador = 1;
    }

    printf ("quer continuar ? ");
printf("s - sim \t n - nao\n");
printf("Escolha: ");
scanf(" %c", &escolha2);
system ("cls");

}while(escolha2 =='s');
  
}
 // jogo ainda em preparaçao
void GousmasWar(){
}

// MENU DOS JOGOS 
int main() {
    int opcao;
    setlocale(LC_ALL, "Portuguese");

    do {
            printf ("  ARCADE CESUPA \n");  
			printf ("\n"); 
			printf ("1:Perguntas e Respostas \n");
            printf ("2:Cobra na Caixa \n");
            printf ("3:Gousmas War  \n"); 
            printf ("0:Sair\n");
            printf(" \n");
   
      printf("Escolha seu jogo: ");
        scanf("%d", &opcao);
         system ("cls");

        switch(opcao) {                       
            case 1:                             
                PerguntasErespostas();                    
                break;                         
                 system ("cls");
            case 2:                            
                cobraNaCaixa();
                break;                               // CHAT GPT
                 system ("cls");                    
            case 3:
                GousmasWar();
                break;
                 system ("cls");
            case 0:
                printf("Saindo...\n");
                break;
            
            
        }

    } while(opcao != 0);

    return 0;
}



