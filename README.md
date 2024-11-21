# Simulación de Ruleta Francesa

Este proyecto implementa una simulación de la ruleta francesa con diferentes estrategias de juego. La simulación está diseñada para evaluar los beneficios de cada estrategia en función de los resultados obtenidos a lo largo del tiempo, donde se enfrentan jugadores y banca.

## Descripción

La simulación se basa en una ruleta con 37 números (0 al 36). Cada 3000 milisegundos, el croupier selecciona un número al azar. Varios jugadores, representados por hilos, realizan apuestas para ganar o perder dinero según el resultado de la ruleta. Los jugadores comienzan con un saldo de **1000 euros** y la banca tiene un saldo inicial de **50,000 euros**.

## Estrategias de Juego

### 1. **Apostar a un número específico**
Cuatro jugadores seleccionan números al azar entre el 1 y el 36 (excluyendo el 0). Cada apuesta cuesta **10 euros**. Si el número elegido coincide con el resultado de la ruleta, el jugador gana **360 euros** (36 veces lo apostado). Si no acierta, pierde los **10 euros** apostados.

### 2. **Apostar a par/impar**
Cuatro jugadores apuestan aleatoriamente a la paridad del número (par o impar). Cada apuesta cuesta **10 euros**. Si el número resultante coincide con la paridad de su apuesta, el jugador gana **20 euros** (el doble de lo apostado). Si no acierta, pierde los **10 euros** apostados.

### 3. **Estrategia de la Martingala**
Cuatro jugadores usan la estrategia de la martingala. Comienzan apostando **10 euros**. Si pierden, doblan la apuesta en la siguiente ronda (20, 40, 80, etc.). Si ganan, su saldo se incrementa en **360 euros**, y la secuencia de apuestas se reinicia en **10 euros**. La banca nunca paga más de lo que tiene disponible en su saldo.

### Reglas Adicionales
- Si el número seleccionado es **0**, todos los jugadores pierden automáticamente y la banca se queda con el total de las apuestas de ese ciclo.
- La banca tiene un saldo inicial de **50,000 euros**, y acepta todas las apuestas, pero no puede pagar más de lo que tiene disponible.

## Funcionamiento de la Simulación

1. **Inicia la simulación**: La ruleta selecciona un número aleatorio cada 3000 milisegundos.
2. **Jugadores realizan apuestas**: Cada jugador elige una estrategia de apuesta (número específico, par/impar, martingala).
3. **Resultados de apuestas**: Se comparan las apuestas de los jugadores con el número de la ruleta. Los jugadores ganan o pierden según el resultado.
4. **Actualización de saldos**: Se actualizan los saldos de los jugadores y de la banca según los resultados de las apuestas.
5. **Registro de resultados**: Se lleva un registro de las ganancias y pérdidas de cada jugador y la banca a lo largo del tiempo.

## Objetivo

El objetivo de esta simulación es observar cómo evolucionan los saldos de los jugadores y de la banca a lo largo del tiempo y determinar qué estrategia es la más efectiva para los jugadores. Esto permitirá evaluar la viabilidad de cada una de las estrategias en el largo plazo.

## Tecnologías Utilizadas

- **Java**: Para la implementación de la simulación y la gestión de hilos (jugadores).
- **Multihilos (Threads)**: Para simular múltiples jugadores simultáneamente.
- **Lógica de Juego**: Simulación de las apuestas y cálculo de resultados.

## Requisitos

- Java 8 o superior.
- Un entorno de desarrollo para ejecutar aplicaciones Java (Eclipse, IntelliJ IDEA, etc.).

## Instrucciones de Uso

1. Clona el repositorio en tu máquina local:

   ```bash
   git clone https://github.com/usuario/ruleta-simulacion.git
