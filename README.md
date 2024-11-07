# PROYECTO INICIAL: Tilting Tiles
# Miembros: ***Julian Santiago Cardenas Cubaque*** y ***Juan Jose Mejia Celis*** 

## Explicacion Diseño:
- Contexto: 
Este proyecto tiene como finalidad representar de manera correcta el puzzle "Tiling Tiles", el cual se basa en una interaccion constante de dos tableros y sus correspondientes fichas. El proyecto se divide en tres paquetes, domain, presentation y test. A partir de estos se rije la funcionalidad del programa donde se divide en estructura logica, interfaz de usuario y testeos de funcionalidad.

- Paquetes:
    1. ***Presentation***: Contiene todo el esquema encargado de la visualizacion del programa frente al usuario, donde podemos ver las clases encargadas de crear y mantener visibles las estructuras y elementos principales del programa, asi como la entrada de conceptos y la formacion de acciones o alteraciones proximas a realizarse.
    2. ***Domain***: Almacena la estructura logica del programa, es decir, guarda todo el ecosistema de metodos y funciones encargadas de realizar todas las acciones del programa, tanto las opciones que tiene el usuario al inicar el proyecto como acciones no visibles que se encargan de realizar calculos y alteraciones mientras se este corriendo el programa.  
    3. ***Test***: Guarda una serie de pruebas realizadas al programa, de tal manera que podemos verificar el correcto funcionamiento de toda la estructura general del codigo, de esta manera se realiza un avance seguro donde nos aseguramos de que se esten cumpliendo los estandares optimos para el funcionamiento del proyecto y tambien detectamos casos en donde no se cumpla con lo esperado. 

- Clases clave:
    1. ***Puzzle***: Esta clase contiene los metodos de mayor importancia del proyecto, ya que es aqui donde se construyen los simientos mas basicos de la estructura del puzzle, ademas de la mayoria de acciones del programa, por lo que esta clase cumple con un papel muy importante tanto en visualizacion como en estructuracion del proyecto.
    2. ***Tile***: Asi como la clase "Puzzle", la clase "Tile" conforma un pilar dentro del proyecto, esta representa las protagonistas del puzzle, es decir, las fichas. Ademas que de aqui surgen sus derivados para que al momento de jugar, el usuario tenga una experiencia mas variada. Esto se logra teniendo en cuenta que la clase "Tile" es una clase abstracta, lo que quiere decir que no se puede isntanciar en otro sitio y sirve como base para poder hacer otras clases, en este caso la variedad de tiles funciona con un sistema de herencia desde la clase "Tile" principal, de esta manera podemos crear varios tipos de Tile.
    3. ***Glue***: La clase de "Glue" juega un papel importante, ya que, brinda la dinamica central del puzzle y se relaciona con la clase "Tile" para formar el concepto central del programa. La idea base del sistema de glue empieza determinando la tile que llevara el glue, a partir de ahi se mira como van a ser afectadas las tiles vecinas, esto puede variar segun su tipo, de ser normales se agruparan para ser movidas juntas. 
       
### Ejecucion casos de prueba:

1. ***Historia de uso, prueba #1***:
   
En un entorno futurista, un ingeniero de mantenimiento de estructuras interactivas, llamado Julián, está probando un nuevo tablero de simulación con fichas inteligentes. Su misión es evaluar cómo responden distintos tipos de fichas a instrucciones de movimiento, obstáculos y elementos en el tablero.

Julián comienza con un tablero vacío, donde cada casilla está inactiva, representada por puntos. Primero, coloca algunas fichas normales (rojas), para probar movimientos básicos. Estas fichas se deslizan en el tablero con facilidad, y Julián observa su reacción al desplazarlas hacia arriba, abajo, izquierda y derecha. Todo parece funcionar bien.

Luego, Julián introduce un nuevo tipo de ficha: fichas fijas (amarillas). Estas fichas son inamovibles y crean barreras en el tablero. Cuando las fichas normales intentan desplazarse en su dirección, se detienen, mostrando que el sistema reconoce correctamente las restricciones.

Más adelante, Julián coloca una ficha áspera (azul), que representa un terreno irregular en el tablero. Quiere comprobar cómo afecta el flujo de las fichas en su entorno, y observa que las fichas normales reaccionan de forma distinta, mostrando la resistencia del terreno áspero.

Finalmente, introduce una ficha freelance (verde), una ficha especial que puede moverse con más libertad y adherirse temporalmente al tablero usando una habilidad de pegado. Julián coloca esta ficha cerca de otras fichas normales, las mueve en diferentes direcciones y experimenta el uso de pegamento en una posición. Además, Julián configura hoyos en el tablero para ver si las fichas caen en ellos cuando pasan sobre estas trampas.

Durante cada prueba, una ventana emergente le permite a Julián decidir si continuar o ajustar el movimiento. Con cada interacción, el sistema se asegura de que las fichas respondan de acuerdo con sus atributos y condiciones.

Al terminar, Julián ha verificado que el tablero y sus elementos cumplen con todos los criterios de interacción, listando posibles mejoras. La simulación ha sido exitosa, y Julián está listo para enviar su informe de pruebas, satisfecho con los resultados.

2. ***Historia de uso, prueba #2***:
   
Juan es un usuario que quiere realizar una prueba más exhaustiva de las funcionalidades del tablero, incluyendo fichas normales, fijas, ásperas, y voladoras. Quiere asegurarse de que las reglas de movimiento y de bloqueo se comporten como se espera.

Juan inicia con un tablero en blanco y añade cuatro fichas: una normal (roja) en (0, 0), una fija (amarilla) en (0, 1), una áspera (azul) en (1, 1), y una voladora (verde) en (2, 2). El objetivo es verificar el movimiento de cada ficha y la correcta aplicación de restricciones.

Primero, mueve el tablero hacia la derecha. La ficha normal se detiene frente a la ficha fija, lo que confirma que las barreras funcionan correctamente. Luego, al mover hacia abajo, la ficha normal baja sin problemas, ya que no tiene obstáculos en esa dirección.

A continuación, Juan intenta mover el tablero hacia la izquierda, y observa que la ficha normal no puede pasar sobre la ficha áspera, ya que esta es inmóvil y bloquea el camino. Finalmente, al mover hacia arriba, comprueba que la ficha voladora evita obstáculos y se comporta de acuerdo con sus propiedades especiales.

Para terminar, Juan realiza una operación de intercambio (exchange) entre la ficha normal y la voladora. Luego, observa el estado final del tablero para confirmar que todas las interacciones se comportaron correctamente según lo esperado.



   
