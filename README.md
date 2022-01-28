#include <stdio.h>
#define comicamisas 15
#define comicalcas 20
#define comitenis 17 

typedef struct est_funcionario //informaçoes sobre cada funcionario
   {
      char salario[10];
      char telefone[15];
      char nome[50];
      char cpf[15];
      char sexo[20];
      char cargo[20];
      char turno[10];
      char email[20];
    } funcionario;
    funcionario f[10];
    int i = 0;

void inserir_informacoes_do_funcionario(funcionario f[]) //funçao que faz preenche as variaveis da struct 
{
 int op = 100; //controle da continuaçao do cadastro
 while(op != 0)
 {
 printf("insira 1 pra cadastrar ou 0 para sair");
 scanf("%d", &op);

 printf("insira o nome:\n");
 fflush(stdin);
 gets(f[i].nome);
 fflush(stdin);
 printf("insira o telefone:\n");
 fflush(stdin);
 gets(f[i].telefone);
 fflush(stdin);
 printf("insira o salario:\n");
 fflush((&_iob[STDIN_FILENO]));
 gets(f[i].salario);
 fflush(stdin);
 printf("insira o cpf:\n");
 fflush(stdin);
 gets(f[i].cpf);
 fflush(stdin);
 printf("insira o sexo:\n");
 fflush(stdin);
 gets(f[i].sexo);
 fflush(stdin);
 printf("insira o cargo:\n");
 fflush(stdin);
 gets(f[i].cargo);
 fflush(stdin);
 printf("insira o turno:\n");
 fflush(stdin);
 gets(f[i].turno);
 fflush(stdin);
 printf("insira o email:\n");
 fflush(stdin);
 gets(f[i].email);
 fflush(stdin);
 i++;
 }
};

void comissao(int camisas, int calcas, int tenis ) //calculo da comissao dos funcionarios
{
 int comi; //recebe o valor da comissao
 comi = camisas * comicamisas + calcas * comicalcas + tenis * comitenis;
 printf("\n%d,00 de comissao\n\n", comi); 
};

int main()
{  
    int camisas, calcas, tenis; //autoexplicativo
    int menu; // controlador do menu
    int i; // controle do cadastro de funcionarios
    do
    {
        printf("digite um numero de 1 a 5");
        printf("\n 1-Cadastro");
        printf("\n 2-Alteracao");
        printf("\n 3-Leitura");
        printf("\n 4-comissao");
        printf("\n 5-Fechar\n");
        scanf("%d", &menu);
        while(menu > 5){
            menu = 0;
        }
        switch (menu)
        {
            case 1:
            inserir_informacoes_do_funcionario(f);
            break;

            case 2:
            printf("\nqual funcionario voce gostaria de alterar os dados ? ");
            scanf("%d", &i);
            printf("insira o nome:\n");
            fflush(stdin);
            gets(f[i].nome);
            fflush(stdin);
            printf("insira o telefone:\n");
            fflush(stdin);
            gets(f[i].telefone);
            fflush(stdin);
            printf("insira o salario:\n");
            fflush((&_iob[STDIN_FILENO]));
            gets(f[i].salario);
            fflush(stdin);
            printf("insira o cpf:\n");
            fflush(stdin);
            gets(f[i].cpf);
            fflush(stdin);
            printf("insira o sexo:\n");
            fflush(stdin);
            gets(f[i].sexo);
            fflush(stdin);
            printf("insira o cargo:\n");
            fflush(stdin);
            gets(f[i].cargo);
            fflush(stdin);
            printf("insira o turno:\n");
            fflush(stdin);
            gets(f[i].turno);
            fflush(stdin);
            printf("insira o email:\n");
            fflush(stdin);
            gets(f[i].email);
            fflush(stdin);
            break;
            case 3:
            printf("escolha qual funcionario voce desejar ver os dados\n");
            scanf("%d" , &i);
            printf("nome: %s \n", f[i].nome);
            printf("telefone: %s \n", f[i].telefone);
            printf("salario: %s \n", f[i].salario);
            printf("cpf: %s \n", f[i].cpf);
            printf("sexo: %s \n", f[i].sexo);
            printf("cargo: %s \n", f[i].cargo);
            printf("turno: %s \n", f[i].turno);
            printf("email: %s \n", f[i].email);
            break;
            case 4:
            printf("insira quantas vendas de\n");
            printf("\ncamisas:");
            scanf("%d", &camisas);
            printf("\ncalcas:");
            scanf("%d", &calcas);
            printf("\ntenis:");
            scanf("%d", &tenis);
            comissao(camisas, calcas, tenis );
            break;
            case 5:
            printf("Ate mais, VOLTE SEMPRE :D");
            break;
        }
    } while (menu <= 4);
}
