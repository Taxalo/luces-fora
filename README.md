# luces-fora

## ⚠️ AVISO
- Luces Fora usa emojis los cuales son usados para representar las luces y los cálculos de distancias para mostrar los índices están pensados con esto enc uenta. Dependiendo de la fuente de la consola o la página de códigos activa (chcp) pueden verse correctamente o no. Para mejor visibilidad usar un IDE como Eclipse o IntelliJ.

## 🧑‍ Colaboradores
- Esta aplicación ha sido diseñada por Quique, Óscar, Fernando, Luís Souto y David.

## 📚 Guía del usuario
- Al iniciar la aplicación nos dará la bienvenida y nos preguntará si queremos empezar el juego o salir de él.
  * > Al seleccionar empezar juego nos preguntará por el tamaño del tablero, en caso de introducir 5 será un 5x5, 10 un 10x10...
  * > Esto generará un tablero totalmente aleatorio con elementos (luces) encendidas y apagadas.
  * > El jugador deberá introducir las coordenadas (X e Y) de un elemento del tablero, lo cual hará que cambien de estado ese elemento y los adyacentes (el superior, el inferior y los de los lados).
  * > El objetivo es que todos los elementos (luces) estén "apagados".
  * > La complejidad aumenta cuanto más grande sea el tablero.
  
## 🛩️ Estructura
- El proyecto está totalmente definido en el archivo [ForaLuz.java](https://github.com/Taxalo/luces-fora/blob/main/src/com/david/ForaLuz.java). Esto es debido a que permite la posibilidad de integrarlo en otros proyectos sin necesidad de que el usuario de ese otro proyecto necesite saber como funciona internamente ni deba crear ningún tipo de física o menú.
- Cuenta con varios métodos como `rellenar()` que es el encargado de rellenar aleatoriaemente el tablero escogido; `mostrarTablero()` que como su nombre indica, muestra el tablero y sus elementos según el estado en el que estén.
- Dos de los métodos más importantes son `esGanador()` y `comprobarCoordenadas()`. Que comprueban continuamente al introducir las coordenadas respectivamente: 1. Si todas las luces están en el estado "apagado"; 2. Si las coordenadas son correctas además de cambiar el estado de las adyacentes mientras comprueba si están dentro del tablero.

## 😎 Diseño
1. Se decidió desarollar todo en una clase y no hacer uso de métodos main para lo dicho anteriormente, mejorar la portabilidad.
2. Crear el método `mostrarAscii()` que muestra el letrero de Luces Fora ha sido la decisión más importante pues ha creado la linea de marca, dándonos la posibilidad de obtener una retribución alta, todo gracias a nuestro asesor financiero y profesional del marketing Fernando.
