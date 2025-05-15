# reto-3-zzzz
mi reto 3, un poco demorado pero acá está
## ¿Cómo funciona?
El algoritmo recorre todos los números desde 2 hasta n, y verifica si cada uno es primo. Para ello, prueba si el número es divisible por algún valor entre 2 y la raíz cuadrada de sí mismo. Si no encuentra ningún divisor, se considera primo.
## Lógica en Pseudocódigo
Solicitar al usuario un número n.

1.Si n es menor que 2, mostrar un mensaje de error.

2.Para cada número x entre 2 y n:

3.Suponemos que x es primo.

*Comprobamos si x tiene algún divisor entre 2 y √x.

*Si encontramos un divisor, x no es primo.

*Si no se encuentra ninguno, imprimimos que x es primo.
## Entrada y Salida
Entrada: Un número entero n.

Proceso: Verificación de cada número desde 2 hasta n usando divisores hasta √x.

Salida: Todos los números primos dentro de ese rango.

## Diagrama de flujo

```mermaid
flowchart TD
    A["Inicio"] --> B["Leer n"]
    B --> C{"¿n < 2?"}
    C -- Sí --> D["Escribir 'Ingrese un número mayor que 1'"]
    C -- No --> E["Para x desde 2 hasta n"]
    E --> F["es_primo := 1"]
    F --> G["Para i desde 2 hasta √x"]
    G --> H{"¿x mod i == 0?"}
    H -- Sí --> I["es_primo := 0"]
    I --> J["Romper bucle"]
    H -- No --> K["Continuar con siguiente i"]
    J --> L["¿Quedan más divisores?"]
    K --> L
    L -- Sí --> G
    L -- No --> M{"¿es_primo == 1?"}
    M -- Sí --> N["Escribir x"]
    M -- No --> O["Continuar con siguiente x"]
    N --> P["Fin"]
    O --> P
    D --> P
