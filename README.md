# GameLabEduc
Aplicativo de jogo let's jump

#include <iostream>
#include <cmath>
#include <cstdlib>
#include <ctime>
#include <inge9>
using namespace std;
	struct point{ 
  		int x,y;
	};

int main() {
   srand(time(0));

  loadImage("background", "https://raw.githubusercontent.com/igorsouzacarvalho88/GameLabEduc/d327597035c9376f2f6774667573d8897ce6db21/Background.png");
  loadImage("doodle", "https://raw.githubusercontent.com/igorsouzacarvalho88/GameLabEduc/8c9d6758c11735dfc7bdfb8b18ca5567d5f0f3b8/doodle.png");
  loadImage("plataforma", "https://raw.githubusercontent.com/igorsouzacarvalho88/GameLabEduc/8c9d6758c11735dfc7bdfb8b18ca5567d5f0f3b8/platform.png");
  waitUntilResourcesLoad();
		Texture t1,t2,t3;
  
    for (int i=0;i<10;i++){
       plataforma[i].x=rand()%400;
       plataforma[i].y=rand()%533;
      }
  
  while (true) {
    drawImage("background", 0, 0);
    drawImage("doodle", 300, 280);
    drawImage("plataforma", 150, 200);
    delay(30);
  }

  return 0;
}
