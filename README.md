import numpy as np
import matplotlib.pyplot as plt

def simular_crecimiento_poblacional(poblacion_inicial, tasa_crecimiento, tiempo):
    poblacion = [poblacion_inicial]
    
    for t in range(1, tiempo):
        nueva_poblacion = poblacion[-1] * (1 + tasa_crecimiento)
        poblacion.append(nueva_poblacion)
    
    return poblacion

if __name__ == "__main__":
    poblacion_inicial = 100
    tasa_crecimiento = 0.05
    tiempo = 50
    
    poblacion = simular_crecimiento_poblacional(poblacion_inicial, tasa_crecimiento, tiempo)
    
    plt.plot(poblacion)
    plt.title("Simulación de Crecimiento Poblacional")
    plt.xlabel("Tiempo")
    plt.ylabel("Población")
    plt.grid(True)
    plt.show()
