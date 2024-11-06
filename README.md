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
    2. ***Tile***: Asi como la clase "Puzzle", la clase "Tile" conforma un pilar dentro del proyecto, esta representa las protagonistas del puzzle, ed decir, las fichas. Ademas que de aqui surgen sus derivados para que al momento de jugar, el usuario tenga una experiencia mas variada.
    3. ***Glue***: La clase de "Glue" juega un papel importante, ya que, brinda la dinamica central del puzzle y se relaciona con la clase "Tile" para formar el concepto central del programa.
       
### Ejecucion casos de prueba:
1. ***Caso prueba***: shouldNotCreateAPuzzleWithAInvalidColor()
   - Un usuario intenta inicializar un puzzle con un tablero (lastBoard) que contiene una ficha con un color no permitido (w).
   - El usuario llama al constructor Puzzle(board, lastBoard) pasando los arreglos board y lastBoard.
   - El constructor revisa cada elemento de board y lastBoard para verificar si contienen colores válidos.
   - Al encontrar el carácter 'w' en lastBoard, el constructor lanza una IllegalArgumentException.
-Resultado esperado: Al encontrar el carácter 'w' en lastBoard, el constructor lanza una IllegalArgumentException.
