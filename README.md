---
layout: page
title: 
---

# Tutorial: jogo Donkey

**Autores**: Renata Lima Ribeiro de Sena

**Conhecimento prévio necessário**: 

**Objetivo de aprendizagem**: 

## Iniciando

Neste tutorial você vai aprender a desenvolver um clone do jogo [Doodle Jump](https://pt.wikipedia.org/wiki/Doodle_Jump), cujo objetivo é guiar o personagem numa série de intermináveis plataformas sem cair.

## Carregando as imagens

Primeiramente vamos carregar as imagens que vamos usar no jogo: o background, a plataforma e o personagem. Para isso, vamos usar a função `loadImage`. Depois disso vamos colocar o background na posição (0, 0) - canto superior esquerdo da tela - usando a função `drawImage`:

```cpp
#include <inge9>
int main() {
  loadImage("background", "https://raw.githubusercontent.com/igorsouzacarvalho88/GameLabEduc/d327597035c9376f2f6774667573d8897ce6db21/Background.png");
  loadImage("doodle", "https://raw.githubusercontent.com/igorsouzacarvalho88/GameLabEduc/8c9d6758c11735dfc7bdfb8b18ca5567d5f0f3b8/doodle.png");
  loadImage("plataforma", "https://raw.githubusercontent.com/igorsouzacarvalho88/GameLabEduc/8c9d6758c11735dfc7bdfb8b18ca5567d5f0f3b8/platform.png");

  drawImage("background", 0, 0);
  
  return 0;
}
```