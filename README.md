# GameLabEduc
Aplicativo de jogo let's jump

#include <iostream>
#include <cmath>
#include <cstdlib>
#include <ctime>
#include <inge9>
using namespace std;

int main() {
   srand(time(0)); - tempo randomico para aparecer as plataformas

int plataformPosition[2]; - Posição inicial das plataformas
  plataformPosition[0]=150; -Tamanho das plataformas
  plataformPosition[1]=150;- Tamanho das plataformas
int doodlePosition[2];    - Posição inicial do Doodle
  doodlePosition[0] = 300; - Tamanho do Doodle se enontra inicial eixo X
  doodlePosition[1] = 280;  - Tamanho do Doodle se enontra inicial eixo Y

  loadImage("background", "https://raw.githubusercontent.com/igorsouzacarvalho88/GameLabEduc/d327597035c9376f2f6774667573d8897ce6db21/Background.png"); Local das imagens e carregamento
  loadImage("doodle", "https://raw.githubusercontent.com/igorsouzacarvalho88/GameLabEduc/8c9d6758c11735dfc7bdfb8b18ca5567d5f0f3b8/doodle.png");Local das imagens e carregamento
  loadImage("plataforma", "https://raw.githubusercontent.com/igorsouzacarvalho88/GameLabEduc/8c9d6758c11735dfc7bdfb8b18ca5567d5f0f3b8/platform.png");Local das imagens e carregamento
  waitUntilResourcesLoad();


  while (true) {


    for(int i=0;i<100;i++){

       drawImage("background", 0, 0);
       drawImage("doodle", doodlePosition[0], doodlePosition[1]);
       drawImage("plataforma", plataformPosition[0], plataformPosition[1]);
       drawText(plataformPosition[0], 100, 300, 22, "black");
       drawText(doodlePosition[0], 300, 300, 22, "black");

       delay(10);
       if (isKeyDown("ArrowLeft")) doodlePosition[0] -=1;
       if (isKeyDown("ArrowRight")) doodlePosition[0] +=1;
       if (isKeyDown("ArrowUp")) doodlePosition[1] -=5;
       if (isKeyDown("ArrowDown")) doodlePosition[1] +=1;
       if ((doodlePosition[0]>plataformPosition[0]+40)&&
         !(doodlePosition[1]+75>plataformPosition[1])){
          doodlePosition[1] +=1;
       }
       clearKey(" ");


     }



  }

  return 0;
}
