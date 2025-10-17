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
    ## Análisis de Datos y Transformada Rápida de Fourier (FFT)

Python es un lenguaje de programación ampliamente utilizado en el ámbito científico debido a sus librerías especializadas. Con respecto al tratamiento de datos, la librería **Pandas** es la herramienta más empleada tanto en ciencias como en ingeniería de datos, por su facilidad para limpiar y estructurar conjuntos de datos.

Pandas está construida sobre **NumPy**, permitiendo trabajar estructuras denominadas **DataFrames**, que son tablas bidimensionales de filas y columnas. Esta estructura facilita el trabajo sobre datos en archivos `.csv`, `.dat`, entre otros. Las funciones más utilizadas incluyen:

- `read_csv()`: para cargar datos desde archivos CSV.  
- `dropna()`: para eliminar datos faltantes.  
- `fillna()`: para completar datos faltantes.  
- `describe()`: para obtener estadísticas descriptivas.  
- `plot()`: para generar visualizaciones rápidas.

Para realizar el análisis pertinente se utilizará la **Transformada Rápida de Fourier (FFT)**, como se mencionó en la introducción. Esta es una herramienta matemática que permite convertir una función del tiempo \(f(t)\) en una representación en frecuencia, mostrando la contribución de cada frecuencia al comportamiento total de la señal.

La **FFT** es una implementación eficiente de la **Transformada de Fourier Discreta (DFT)**, definida como:

\[
X[k] = \sum_{n=0}^{N-1} x[n] \, e^{-j 2 \pi k n / N}, \quad k = 0,1, \dots, N-1
\]

donde:  
- \(N\) es el número total de muestras de la señal.  
- \(x[n]\) es la señal en el tiempo.  
- \(X[k]\) representa la amplitud y fase de la frecuencia \(k\)-ésima.  
- \(j\) es la unidad imaginaria.

Esta herramienta permite estudiar las variaciones temporales de las mareas, identificando los componentes periódicos y sus frecuencias dominantes, como las **mareas semidiurnas (12 h)** o **diurnas (24 h)**.

## 🔨Metodología
    El procedimiento se divide en dos etapas principales:
1. **Tratamiento de datos**
2. **Análisis de datos**
La obtención de los datos se logró mediante el director del Centro de Investigación
del Mar y Limnología de la Universidad de Costa Rica, por sus siglas CIMAR. 
Dichos datos provienen de dos sensores distintos colocados en Bahía Herradura, en el
pacífico costarricense. Estos sensores son:
- "YSI WaterLog Nile Water Level Radar Series 517"
- "Tide Sensor 5217/5217R"
El primero de ellos es un sensor por radar que funciona sin contacto directo con el agua.
Emite pulsos de radar/microondas hacia la superficie del agua, estos se reflejan y luego mide 
el tiempo que tarda en volver el eco. Tiene un rango de hasta 70m lo que lo hace útil 
para distintos tipos de agua.

El segundo sensor es un dispositivo que mide distintas condiciones de marea como presión,
presión de marea, temperatura y lo más importante para el presente proyecto, nivel de marea. 
Este dato es medido indirectamente mediante la presión hidroestática, detectando cuánto peso
ejerce el agua sobre el sensor.

Tras obtener los datos en formato .dat de ambos dispositivos, se procede a realizar una limpieza 
típica del documento mediante la libreria Pandas. Este proceso incluye eliminar valores atípicos
relacionados con la calibración y fallas de los equipos, conversión de unidades al SI y visualizaciones 
iniciales de las variables pertinentes con gráficos temporales.

El análisis de datos se realiza mediante la FFT aplicada a la señal procesada para obtener
el espectro de frecuencias, las cuales se deben identificar por las dominantes astronómicas M2, S2,
K1, O1, etc. Después, se convierte la frecuencia a periodos para una visualización de amplitudes vs periodos.
La relación física de las componentes con las mareas astronómicas permitirá finalmente, realizar las predicciones 
temporales pertinentes.

