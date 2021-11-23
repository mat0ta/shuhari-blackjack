# Shu-Ha-Ri del juego de Blackjack
Este trabajo lo hemos hecho:
[Martín](https://github.com/mat0ta),
[Rubén](https://github.com/rnoguer22) y 
[Diego](https://github.com/Diegodesantos1)

El link del repositorio es este: [Repositorio](https://github.com/mat0ta/shuhari-blackjack)


EL otro grupo nos ha pasado el código vía email en un archivo txt, algo un poco arcaico comparado con las facilidades que ofrece github para compartir código.

El código que han empleado los compañeros del otro grupo es el siguiente el cual se parece bastante al código que nos proporcionó Rubén, además se llama exactamente igual: 23__01__Introduccion.py

Este código en primer lugar importa la librería "random" para poder aleatorizar parte del código.

Crea el diccionario de las cartas, crea una lista a partir de la librería creada. Después selecciona 4 cartas aleatorias, 2 para la banca y 2 para el jugador, printeando las cartas junto a la suma de los valores de las mimas.

<br>
<img height="780" src="./Shu-Ha-Ri.drawio (1).png" />
<br>


Para verlo más claro pincha aquí: [Flowchart](https://github.com/mat0ta/shuhari-blackjack/blob/main/Shu-Ha-Ri.drawio%20(1).png)


```
from random import choice, sample

cartas = {
    chr(0x1f0a1): 11,
    chr(0x1f0a2): 2,
    chr(0x1f0a3): 3,
    chr(0x1f0a4): 4,
    chr(0x1f0a5): 5,
    chr(0x1f0a6): 6,
    chr(0x1f0a7): 7,
    chr(0x1f0a8): 8,
    chr(0x1f0a9): 9,
    chr(0x1f0aa): 10,
    chr(0x1f0ab): 10,
    chr(0x1f0ad): 10,
    chr(0x1f0ae): 10,
}

for carta, valor in cartas.items():
    print("la carta {} vale {}".format(carta, valor))

print("Empieza el Black Jack")
lista_cartas = list(cartas)

main_jugador = sample(lista_cartas, 2)
score_jugador = sum(cartas[carta] for carta in main_jugador)
print("Te han tocado las cartas: {} {} , y su puntuación es {}.".format(main_jugador[0],
                                                          main_jugador[1],
                                                          score_jugador))

main_banca = sample(lista_cartas, 2)
score_banca = sum(cartas[carta] for carta in main_banca)
print("La banca tiene las cartas: {} {} , y su puntuación es {}.".format(main_banca[0],
                                                          main_banca[1],
                                                          score_banca))

```
---
Para mejorar el código presentado añadidríamos varias funciones:
- Una función para que el jugador pueda jugar al Blackjack
- Añadiríamos una clase en la que tener todo el código organizado
- Cada vez que se de una carta, quitar esa misma carta de la lista para que no se repita
