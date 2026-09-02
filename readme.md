## Compilar
Para gerar o arquivo executável *(o jogo)* basta executar o arquivo 'compila'

Esse arquivo envia o código-fonte do arquivo *game.c* para o compilador tinyCC\
(Tiny C Compiler).

O nome do arquivo com código deve ser game.c

No desenvolvimento de software é comum errar e tentar de novo.\
Caso haja algum erro no código o 'compila' irá falhar.\
As regras da linguagem C são muitas e são rígidas.

O **compila.bat** exibe uma descrição do erro (em inglês) caso o executável não possa ser gerado.\
Procurar na internet pela descrição do erro exibida é uma boa iniciativa.

## Código Mínimo (entrando no modo gráfico)
```c
#include "poly/poly.h"
main(){
	setvideomode();
	while(!keystate(KEY_ESCAPE)){

		waitvbl();
	}
}
```

## Poly
Esse é um software resignadamente educacional e os jogos resultantes tem limitações.\
Bons softwares geralmente exploram alguns limites e esse é complacente.

O objetivo desse software é incentivar a comunidade brasileira de jogos.\
Esse software atua na divulgação do fato que escrever código é legal.

## Funções Poly
```c
void setcolor(int color); //determina a cor a ser utilizada
int getcolor(); //devolve a cor
void putpixel(int x,int y,int color); //coloca um pixel na tela
void line(int x1,int y1,int x2,int y2); //linha na tela
void rectangle(int x,int y,int w,int h);
void bar(int x,int y,int w,int h); //retangulo preenchido
void circle(int x,int y,int r);
void fillcircle(int x,int y,int r);
void ellipse(int x,int y,int rx,int ry);
void fillellipse(int x,int y,int rx,int ry);
void drawpoly(int* points_xy,int count); //poligono pelos vertices
void fillpoly(int* points_xy,int count);
void blitInt(int n,int x,int y); //exibe numero inteiro
int keystate(enum key); //tecla pressionada
int rand(void); //numero aleatorio
void sleep(int duration); //intervalo entre um frame e outro
```

## Site Oficial
https://RodrigoSchioMuniz.github.io/procedimentos/res/20/sitePoly