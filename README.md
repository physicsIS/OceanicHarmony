![Banner](./herradura_picture.jpg)
 <!-- 🏷️ Badges informativos del proyecto -->
![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)
![FFT](https://img.shields.io/badge/Análisis-FFT-orange?logo=waveform)
![Datos](https://img.shields.io/badge/Datos-Bahía%20Herradura-00bfa5?logo=databricks)
![Ubicación](https://img.shields.io/badge/País-Costa%20Rica-009688?logo=earth)
![Estado](https://img.shields.io/badge/Estado-En%20Desarrollo-yellow?logo=progress)
![Licencia](https://img.shields.io/badge/Licencia-MIT-green?logo=open-source-initiative)

# 🌊 Análisis Espectral de la Marea en Bahía Herradura 🌊
## Descripción del proyecto
    El presente proyecto propone realizar un análisis espectral de la marea del Océano Pacífico de Costa Rica, específicamente 
    en Bahía Herradura. Esto mediante el uso de métodos de análisis armónico y trasnformadas rápidas de Fourier (FFT).
    Se busca identificar las principales componentes armónicas y discutir sus posibles aplicaciones en dinámica costera,
    además de realizar predicciones del nivel del mar.
    "If you can not explain it simply, you do not understand it well enough" -Albert Einstein
## 📘 Contenidos
1. [Introducción](#-introducción)
2. [Marco Teórico](#-Marco-teórico)
3. [Metodología](#-metodología)
4. [Resultados](#-resultados)
5. [Estructura del repositorio](#-estructura-del-repositorio)
6. [Ejemplo de ejecución](#-ejemplo-de-ejecución)
7. [Créditos](#-créditos)
## 🔎Introducción
    Se aplicará la transformada rápida de Fourier (FFT) a los datos del registro horario del nivel del mar (proporcionados por el CIMAR)
    para descomponer la señal en sus componentes armónicas fundamentales M2, S2, K1, O1, entre otras. Una vez hecho este análisis,
    se procederá a realizar pronósticos de los niveles del mar en Bahía Herradura, Costa Rica. 
## 📚 Márco teórico
    Python es un lenguaje de programación ampliamente utilizado en el ámbito
    científico debido a sus librerias especializadas. Con respecto al tratamiento
    de datos la librería "Pandas" es la herramienta más empleada tanto en las áreas 
    científicas como en ingeniera de datos por su facilidad a la hora de manipular,
    limpiar y estructuras conjuntos de datos. 
    \\ Pandas esta construida sobre Numpy, permitiendo trabajar estructuras de datos 
    denominadas "DataFrames" las cuales son tablas bidimensionales con etiquetas en filas
    y columnas. Esta estructura facilita el trabajo sobre datos en formatos como .csv, .txt,
    .dat, entre otros. Las funciones más utilizadas suelen ser aquellas para importar los datos 
    como `read_csv()`, eliminar o completar datos con `dropna()`,` interpolate()`, y aquellas que
    permiten obtener las estadísticas `describe()`,` plot()`.
    \\Para realizar el análisis pertinete se utilizará la Transformada Rápida de Fourier
    como se mencionó en la introducción. Esta es una herramienta matemática que convierte
    una función del tiempo f(t) en una representación en frecuencia F(ω) permitiendo identificar
    la contribución de cada frecuencia al comportamiento total de la señal. 
    Su representación continua se define como: 
        ![Transformada de Fourier](https://latex.codecogs.com/svg.image?F(\omega)=\int_{-\infty}^{\infty}f(t)\exp(-i\omega%20t)\,dt)


## 🔨Metodología
    Se

