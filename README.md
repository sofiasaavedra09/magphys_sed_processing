# MAGPHYS SED Processing

## Descripción

Este proyecto automatiza el procesamiento de archivos de salida generados por MAGPHYS para visualizar la Distribución de Energía Espectral (SED) de múltiples galaxias. El notebook procesa automáticamente los archivos `.dat`, `.fit` y `.sed`, extrae los parámetros físicos más relevantes y genera una figura para cada objeto.

## Objetivo

El objetivo de este proyecto es demostrar el desarrollo de un flujo de trabajo automatizado para el procesamiento de datos astronómicos utilizando Python. Más que realizar un análisis científico completo, el notebook busca reemplazar tareas repetitivas por un proceso reproducible, modular y fácilmente escalable a múltiples archivos de salida de MAGPHYS. Además, organiza el código mediante funciones reutilizables y facilita el procesamiento de conjuntos de datos astronómicos sin intervención manual.

## Características

- Procesamiento automático de múltiples archivos de salida de MAGPHYS.
- Lectura y extracción de información desde archivos `.dat`, `.fit` y `.sed`.
- Reconstrucción de las componentes atenuada y no atenuada de la distribución de energía espectral (SED).
- Generación automática de una figura por cada galaxia procesada.
- Organización del código en funciones reutilizables y documentadas.
- Uso de rutas relativas para facilitar la ejecución en distintos equipos.

## Estructura del repositorio

```text
magphys_sed_processing/
│
├── data/                         # Archivos de entrada (.dat, .fit, .sed)
├── plots/                        # Figuras generadas automáticamente
├── magphys_sed_processing.ipynb  # Notebook principal
└── README.md                     # Documentación del proyecto
```

## Requisitos y ejecución

### Requisitos

- Python 3.
- Jupyter Notebook o Visual Studio Code con la extensión de Jupyter.
- Bibliotecas:
  - numpy
  - matplotlib
  - pandas
  - os

### Ejecución

1. Clonar o descargar este repositorio.
2. Colocar los archivos `.fit` y `.sed` en la carpeta `data/`.
3. Abrir el notebook `magphys_sed_processing.ipynb`.
4. Ejecutar todas las celdas en orden.
5. Las figuras generadas se almacenarán automáticamente en la carpeta `plots/`.

## Limitaciones y trabajo a futuro

Este proyecto fue desarrollado con un conjunto reducido de archivos de salida de MAGPHYS cuyo objetivo es demostrar la automatización del procesamiento, más que realizar un análisis astrofísico completo.

Los archivos incluidos en la carpeta `data` corresponden a tres copias de los archivos de ejemplo `example.fit` y `example.sed`, a las que se asignaron identificadores ficticios únicamente para demostrar que el flujo de trabajo procesa múltiples objetos de forma automática. Por esta razón, los resultados obtenidos no representan galaxias diferentes ni deben interpretarse como un análisis científico.

La visualización presentada corresponde a una versión simplificada de la distribución de energía espectral, ya que el archivo `filters.dat`, necesario para incorporar la respuesta de los filtros observacionales, no estuvo disponible. En caso de disponer de dicho archivo, junto con un conjunto completo de datos generado por MAGPHYS, el notebook puede extenderse fácilmente para incluir esta información en las figuras.

Como trabajo futuro, el flujo de procesamiento puede adaptarse para analizar conjuntos de datos más grandes o incorporar nuevas visualizaciones y parámetros físicos extraídos de las salidas de MAGPHYS.

## Créditos y agradecimientos

La función utilizada para cargar y visualizar los histogramas de probabilidad fue desarrollada originalmente como parte de un trabajo colaborativo realizado durante mi formación universitaria. En este proyecto fue adaptada e integrada al flujo de procesamiento automatizado.

Los archivos de ejemplo `.fit` y `.sed` utilizados en este repositorio provienen del repositorio **magphys-read-output** de astronomeralex y se incluyen únicamente con fines demostrativos, respetando los términos de la licencia del proyecto original:

https://github.com/astronomeralex/magphys-read-output
