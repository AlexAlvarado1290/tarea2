# tarea2
imprimir patrones de * dependiendo de la opcion ingresada por el usuario

## Algoritmo tarea2 en Pseudocódigo

Definir `opcion` Como Entero
Definir `asterisco` como Cadena

`asterisco` = "*"
Escribir "Seleccione una opción:"
Escribir "1. diseño 1"
Escribir "2. diseño 2"
Escribir "3. diseño 3"
Escribir "4. diseño 4"
Escribir "Ingrese su opción:"
Leer `opcion`

Segun `opcion` Hacer
    Caso 1:
        Para `i` <- 1 Hasta 5 Con Paso 1 Hacer
            Para `j` <- 1 Hasta `i` Con Paso 1 Hacer
                Escribir Sin Saltar `asterisco`
            FinPara
            Escribir ""
        FinPara
    Caso 2:
        Para `i` <- 1 Hasta 5 Con Paso 1 Hacer
            Para `j` <- 1 Hasta 5 Con Paso 1 Hacer
                Si `j` <= 5 - `i` Entonces
                    Escribir Sin Saltar " "
                Sino
                    Escribir Sin Saltar `asterisco`
                FinSi
            FinPara
            Escribir ""
        FinPara
    Caso 3:
        Para `i` <- 1 Hasta 5 Con Paso 1 Hacer
            Para `j` <- 1 Hasta 5 Con Paso 1 Hacer
                Si `j` < `i` Entonces
                    Escribir Sin Saltar " "
                Sino
                    Escribir Sin Saltar `asterisco`
                FinSi
            FinPara
            Escribir ""
        FinPara
    Caso 4:
        Para `i` <- 1 Hasta 5 Con Paso 1 Hacer
            Para `j` <- 1 Hasta 5 Con Paso 1 Hacer
                Si `j` <= 5 - `i` + 1 Entonces
                    Escribir Sin Saltar `asterisco`
                Sino
                    Escribir Sin Saltar " "
                FinSi
            FinPara
            Escribir ""
        FinPara
    De Otro Modo:
        Escribir "Opción no válida"
FinSegun

FinAlgoritmo

## Algoritmo tarea2 en C++

```cpp
#include <iostream>

int main() {
    int opcion;
    std::cout << "Seleccione una opción:" << std::endl;
    std::cout << "1. diseño 1" << std::endl;
    std::cout << "2. diseño 2" << std::endl;
    std::cout << "3. diseño 3" << std::endl;
    std::cout << "4. diseño 4" << std::endl;
    std::cout << "Ingrese su opción: ";
    std::cin >> opcion;

    char asterisco = '*';

    if (opcion == 1) {
        for (int i = 1; i <= 5; i++) {
            for (int j = 1; j <= i; j++) {
                std::cout << asterisco;
            }
            std::cout << std::endl;
        }
    } else if (opcion == 2) {
        for (int i = 1; i <= 5; i++) {
            for (int j = 1; j <= 5; j++) {
                if (j <= 5 - i) {
                    std::cout << ' ';
                } else {
                    std::cout << asterisco;
                }
            }
            std::cout << std::endl;
        }
    } else if (opcion == 3) {
        for (int i = 1; i <= 5; i++) {
            for (int j = 1; j <= 5; j++) {
                if (j < i) {
                    std::cout << ' ';
                } else {
                    std::cout << asterisco;
                }
            }
            std::cout << std::endl;
        }
    } else if (opcion == 4) {
        for (int i = 1; i <= 5; i++) {
            for (int j = 1; j <= 5; j++) {
                if (j <= 5 - i + 1) {
                    std::cout << asterisco;
                } else {
                    std::cout << ' ';
                }
            }
            std::cout << std::endl;
        }
    } else {
        std::cout << "Opción no válida" << std::endl;
    }

    return 0;
}

## Algoritmo tarea2 en Python

```python
def imprimir_patron(opcion):
    asterisco = "*"

    if opcion == 1:
        for i in range(1, 6):
            for j in range(1, i + 1):
                print(asterisco, end="")
            print()
    elif opcion == 2:
        for i in range(1, 6):
            for j in range(1, 6):
                if j <= 5 - i:
                    print(" ", end="")
                else:
                    print(asterisco, end="")
            print()
    elif opcion == 3:
        for i in range(1, 6):
            for j in range(1, 6):
                if j < i:
                    print(" ", end="")
                else:
                    print(asterisco, end="")
            print()
    elif opcion == 4:
        for i in range(1, 6):
            for j in range(1, 6):
                if j <= 5 - i + 1:
                    print(asterisco, end="")
                else:
                    print(" ", end="")
            print()
    else:
        print("Opción no válida")

opcion = int(input("Seleccione una opción:\n1. diseño 1\n2. diseño 2\n3. diseño 3\n4. diseño 4\nIngrese su opción: "))
imprimir_patron(opcion)

