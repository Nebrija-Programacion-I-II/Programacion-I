# Práctica I

Se desea realizar un juego del ahorcado
Este juego del ahorcado va a ser algo simple (ya lo complicaremos). La palabra a adivinar va a ser siempre la misma: "avion".

## Paso 1 (2 puntos)
Crear un programa que pida al usuario una letra. El programa de indicar si esa letra forma parte de la palabra elefante o no.

## Paso 2 (3 puntos)
El jugador va a tener 7 vidas.

Si cuando el usuario introduce la letra no forma parte de la palabra "avion", debe decrementar una variable, llamada "vidas", cuyo valor inicial es 6. Cada vez que el usuario introduzca una letra el programa debe decir:

`la letra yyy forma parte que la palabra secreta, te quedan xxx vidas` 

o bien 

`la letra yyy no forma parte que la palabra secreta, te quedan xxx vidas`

## Paso 3 (3 puntos)
Para mostrar lo que el usuario ha adivinado trabajaremos con una variable tipo *string* que llamaremos adivinada: `std::string adivinada{"*****"};` que inicialmente serán todo asteríscos (y tiene el mismo número de asteríscos que letras tiene *avion*, es decir, 5).

Cada vez que el usuario introduzca una letra:
  1. Comprobar si esa letra pertenece a "elefante".  
  2. En caso de que pertenezca ver su posición.
  3. Comprobar el valor que hay en esa posición en la variable *adivinada*.
  4. Si hay un * sustituir el * por la letra adivinada.

## Paso 4 (2 puntos)
Dibujar por pantalla el monigote ahorcandose cada vez que va perdiendo vidas.

```
   |
   O
  /|\
  / \
```

## NOTA
La estructura del programa es la siguiente:

```cpp
#include <string>
#include <iostream>

int main(){
  std::string palabra{"avion"};
  std::string adivinada{"*****"};
  int vidas{7};
  while(vidas > 0){
    
    // EL PROGRAMA VA AQUI

    if(adivinada == palabra){
      std::cout << "Has ganado\n";
      return 0;
    }
  }

  std::cout << "Oh, oh\n\n";
  std::cout << 
  " |\n" <<
  " O\n" <<
  "/|\\\n"<<
  "/ \\\n"; 


  return 0;
}
```