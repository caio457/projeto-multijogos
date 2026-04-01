# projeto-multijogos



#include <stdio.h>
#include <locale.h>
#include <stdlib.h>
int main ()
{
	
char jg , opcao ;
setlocale(LC_ALL, "Portuguese");

//printf ("  TÍTULO DO JOGO \n");
//printf ("\n");

//printf ("1:Perguntas e Respostas \n");
//printf ("2:Cobra na Caixa \n");
//printf ("3:Gousmas War  \n"); 
//printf ("4:Sair\n");
//printf(" \n");
//printf ("escolha seu jogo : ");
//scanf(" %c",&jg);
//if (jg == '4')
//{
//	return 0 ;
//}
//else 
	







//system("cls");


char r1 , r2 , r3 , r4 , r5;
char escolha ;

	
	
do{	
	printf ("  TÍTULO DO JOGO \n");
printf ("\n");

printf ("1:Perguntas e Respostas \n");
printf ("2:Cobra na Caixa \n");
printf ("3:Gousmas War  \n"); 
printf ("4:Sair\n");
printf(" \n");
printf ("escolha seu jogo : ");
scanf(" %c",&jg);
if (jg == '4')
{
	return 0 ;
}
	
	
	
	
	system("cls");
	

printf ("Qual destes NÃO é um sistema operacional?\n");
printf("A-linux\n");
printf("B-windows\n");
printf("C-macOS\n");
printf("D-chrome\n");        
printf("Escolha: ");                                   //pergunta 1
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
printf("Escolha: ");
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
printf("Escolha: ");
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
printf("Escolha: ");
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
printf("Escolha: ");
scanf(" %c", &r5);
if(r5 == 'C'||r5 == 'c' )
{
	printf ("resposta correta ");
}
else 
printf ("resposta incorreta");




printf ("quer continuar ? ");
printf("s - sim \t n - nao\n");
printf("Escolha: ");
scanf(" %c", &escolha);
system ("cls");

}while(escolha =='s');








return 0 ;
}
















