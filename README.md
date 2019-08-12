# hello world
estudo

olá estou iniciando agora, tudo bem.
int a= 1x12345678;

#include <iostream.h>
void main(void)
{
 cout << “Digite os valores (negativo finaliza): “;
 float soma = 0;
 while( true ) {
 float valor;
 cin >> valor;
 if( valor<0 ) break;
 soma += valor;
 }
 cout << “\nSoma: “ << soma << endl;
}
Podemos até declarar um contador diretamente dentro de uma instrução for :
Exemplo 1.9:
#include <iostream.h>
void main(void)
{
 cout << “Contagem regressiva: “ << endl;
 for(int i=9; i>=0; i--)
 cout << i << endl;
} 
Um C melhorado 5
O operador de resolução de escopo (::) nos permite acessar uma variável global, mesmo
que exista uma variável local com o mesmo nome.
Exemplo 1.10:
#include <iostream.h>
int n=10;
void main(void)
{
 int n=20;
 {
 int n=30;
 ::n++; // altera variável global
 cout << ::n << “ “ << n << endl;
 }
 cout << ::n << “ “ << n << endl;
}
A saída produzida por esse programa é a seguinte:
11 30
11 20
