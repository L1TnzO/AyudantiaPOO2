Enzo Loren

Análisis de las clases y relaciones para el juego de Blackjack:

Clase Carta:
Atributos:
valor: representa el valor de la carta, puede ser un número del 1 al 10 o una letra representando a la Jota, Quina, Kaiser o As.
pinta: representa la pinta de la carta, puede ser Corazón, Trébol, Diamante o Pica.
Métodos:
getValor(): devuelve el valor numérico de la carta según las reglas del juego (10 para las letras y 11 para el As).
toString(): devuelve una representación en cadena de la carta.
Clase Baraja:
Atributos:
cartas: una lista que almacena objetos de la clase Carta, representa las cartas en la baraja.
Métodos:
Baraja(): constructor que inicializa la lista de cartas de la baraja con todas las posibles combinaciones de valor y pinta.
mezclar(): ordena aleatoriamente las cartas en la lista.
repartir(): devuelve la primera carta de la lista y la elimina de la misma.
Clase Jugador:
Atributos:
nombre: una cadena de caracteres que identifica al jugador.
mano: una lista que almacena objetos de la clase Carta, representa las cartas en la mano del jugador.
Métodos:
pedirCarta(Baraja baraja): recibe un objeto de la clase Baraja como parámetro y añade una carta de la baraja a la mano del jugador.
plantarse(): indica que el jugador no quiere recibir más cartas.
calcularPuntaje(): suma los valores numéricos de las cartas en la mano del jugador y devuelve el resultado.
mostrarMano(): muestra todas las cartas en la mano del jugador.
Clase Crupier:
Hereda de la clase Jugador.
Atributos:
No tiene atributos adicionales.
Métodos:
mostrarCarta(): devuelve la primera carta en la mano del crupier sin eliminarla de la lista.
mostrarMano(): muestra la primera carta en la mano del crupier.
Clase Juego:
Atributos:
baraja: un objeto de la clase Baraja, representa la baraja de cartas utilizada en el juego.
crupier: un objeto de la clase Crupier, representa al crupier del juego.
jugadores: una lista que almacena objetos de la clase Jugador, representa los jugadores en el juego.
Métodos:
iniciar(): crea e inicializa los atributos de la clase, como mezclar la baraja.
repartirInicial(): reparte dos cartas a cada jugador y al crupier utilizando el método pedirCarta() de cada uno.
jugar(): permite a cada jugador decidir si quiere pedir más cartas o plantarse utilizando los métodos pedirCarta() y plantarse() respectivamente.
determinarGanador(): compara los puntajes de cada jugador y del crupier utilizando el método calcularPuntaje() de cada uno, y devuelve el nombre del ganador o un mensaje indicando si hay empate o si todos han perdido.
agregarJugador(Jugador jugador): agrega un objeto de la clase Jugador a la lista de jugadores.

Cambios observados entre la implementación inicial y final del programa:

Se agregó la clase Crupier, que hereda de la clase Jugador, para representar al crupier del juego.
Se modificó el método mostrarMano() en la clase Crupier para mostrar solo la primera carta en la mano.
Se realizaron ajustes menores en los nombres de variables y en los mensajes de salida para mejorar la legibilidad y la interacción con el usuario.
Se realizaron adiciones menores en los métodos toString() de la clase Carta y mostrarManoCompleta() en la clase Jugador para brindar información más completa.
