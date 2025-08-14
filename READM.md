# //======================================================
//          Sistema de Medición de Distancias en Carro
//                 Versión 1.0 - 2025
//======================================================

#include <iostream>
#include <cmath>

# // Definición de constantes
const double PI = 3.141592653589793;
const double RADIO_RUEDA = 0.35;  // Radio de la rueda en metros (ejemplo)

# // Función para calcular la distancia recorrida basada en el número de revoluciones
double calcularDistancia(int revoluciones) {
    // Distancia = Perímetro de la rueda * Número de revoluciones
    double perimetro = 2 * PI * RADIO_RUEDA;
    return perimetro * revoluciones;
}

# // Función principal
int main() {
    # // Variables de entrada y salida
    int revoluciones;  // Número de revoluciones de la rueda
    double distanciaRecorrida;  // Distancia total recorrida en metros

   # // Título del programa
    std::cout << "===============================" << std::endl;
    std::cout << "  Sistema de Medición de Distancia" << std::endl;
    std::cout << "===============================" << std::endl;

   # // Solicitar la cantidad de revoluciones
    std::cout << "Introduce el número de revoluciones de la rueda: ";
    std::cin >> revoluciones;

   # // Verificar que la entrada sea válida
    if (revoluciones < 0) {
        std::cout << "El número de revoluciones no puede ser negativo." << std::endl;
        return 1;  // Código de error
    }

  #  // Calcular la distancia
    distanciaRecorrida = calcularDistancia(revoluciones);

  #  // Mostrar el resultado
    std::cout << "La distancia recorrida es: " << distanciaRecorrida << " metros." << std::endl;

    return 0;
}



