**Organización de computadores**
**Proyecto 4 - Programación**
**2026-2**

# Integrantes
* Ana Isabella Gómez García
* Juan Pablo López Lidueña

## Aportes
| Nombre | Usuario GitHub | Aportes principales |
|---|---|---|
| Ana Isabella | Taegrito | Encargada del apartado grafico y los menus. |
| Juan Pablo | 4Lonus | Encargado de la logica de las carreras obstaculos y VM. |

# Compilación y ejecución
## Requisitos
Para compilar y ejecutar este proyecto se necesita:
- Jack compiler de Nand2Tetris
- VM Emulator de Nand2Tetris
- Los archivos fuente

## Compilación
1. Clonar el repositorio desde github:
   `bash
   git clone https://github.com/Taegrito/Proyecto4Organizacion.git
   `
2. Ingresar a la carpeta del proyecto
  `cd Proyecto4`
3. Compilar los archivos Jack
  `tools/JackCompiler.sh RUTA/proyecto4`
4. Verificar que se hayan generado los archivos `.vm` correspondientes a la clase jack.
   
## Ejecución
1. Abrir VM Emulator.
2. Cargar la carpeta del proyecto 4.
3. Seleccionar la velocidad máxima de ejecución.
4. Presionar `Run` para iniciar el programa.
   
# Controles
Los controles del juego son los siguientes:
| Tecla | Función |
|---|---|
| Flecha arriba | Mover el carro al carril superior |
| Flecha abajo | Mover el carro al carril inferior |
| P | Pausar o reanudar la partida |
| R | Reiniciar la partida |
| ESC | Salir del juego |
| 1 | Seleccionar carrera de 50 pasos |
| 2 | Seleccionar carrera de 100 pasos |
| 3 | Seleccionar carrera de 150 pasos |
El movimiento del carro se realiza entre tres carriles. Durante la partida, las entradas del teclado se consultan sin detener el ciclo del juego.

# Diseño de clases
## Main.jack
Es el punto de entrada del programa. Crea el objeto `Pantalla`, ejecuta la interfaz y libera sus recursos cuando termina el juego.

## Pantalla.jack
Es la encargada de la interacción entre la interfaz y el usuario y de la interfaz visual.

Sus principales responsabilidades son:
* Mostrar el menú inicial y seleccionar la distancia.
* Leer las entradas del teclado.
* Controlar la pausa, el reinicio y la salida.
* Dibujar el carro, los obstáculos y los tres carriles.
* Mostrar las vidas, los puntos y el progreso.
* Presentar los resultados de la partida.
* Eliminar la memoria utilizada por los Sprites.

## TipoObstaculo.jack
Es el encargado de describir los tipos de obstaculos, los cuales serán posteriormente referenciados por `Obstaculo.jack`.

## Obstaculo.jack
Es el encargado de 

## Carrera.jack


# Rutinas VM
## Aleatorio.vm
Solo tiene 2 funciones.
* `semilla(int)`: inicializa un numero entero (de 16 bits) como la semilla (seed).
* `siguiente()`: multiplica la semilla por 5 y le suma 3 al resultado (con la intención de generar un numero pseudoaleatorio).

## Grafico.vm (por implementar)
Solo esta compuesto de una funcion.
* `dibujarCelda(int, int, array)`: imprime en la pantalla un sprite en una celda (de 16x16 pixeles) de una malla que divide a la pantalla 16x32 durante el juego.

# Uso de IA
Se utilizó ChatGpt, Claude y DeepSeek v4.1 flash como apopyo durante el desarrollo del proceso, a través de la correción de errores que se presentaron en el código. No se usó LLMs para generar ninguna parte del codigo, solo de manera conceptual o para aclarar dudas tecnicas, y todas las correcciones fueron implementadas a mano por los integrantes.
