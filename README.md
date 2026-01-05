# Documentación del Proyecto

## Participantes
Andrea Sacristán
Isay González

## Descripción del Proyecto

El proyecto se centra en el análisis de datos meteorológicos del dataset del Sistema de Información Agroclimático Regional (SIAR). Está escrito en python en un sólo archivo de jupyter notebook.

## Librerías Necesarias
Las librerías empleadas en el proyecto son las siguientes:

- **pandas**
- **numpy**
- **matplotlib**
- **seaborn**
- **scikit-learn (sklearn)**
- **scipy**
- **mlxtend**
- **datetime**
- **glob**
- **sys**
- **warnings**

## Archivos del proyecto
- **work.csv**: Archivo con el set de datos a analizar
- **Weather_analysis.ipynb**: Cuaderno de análisis con los algoritmos
- **readme.md**: Documentación del proyecto
- **work_with_season.csv**: Archivo con el set de datos postprocesado, limpio y únicamente con los datos de análisis


## Ejecución del proyecto

El proyecto está preparado para ser ejecutado en un entorno jupyter notebook, es necesario ejecutar el cuaderno de análisis Weather_analysis.ipynb e importar las librerías externas para su ejecución. El archivo con el set de datos original work.csv, se modifica durante la ejecución del script, por lo que es recomendable copiar el archivo original antes de ejecutar el script, que se encuentra en /origen a la carpeta raiz del proyecto.

## Secciones del proyecto

La estructura del cuaderno principal de análisis es la siguiente:

 **Análisis del dataset SIAR** 

 **1. Filtrado de Columnas**
El algoritmo guarda únicamente las columnas que son necesarias para el análisis.

 **2. Añadir Estación del Año**
Después de limpiar las columnas no necesarias, este algoritmo calcula la estación del año en base a la columna fecha en la que se tomó la medición.

 **3. Limpieza de los datos**
Este algoritmo elimina outliers y sustituye valores nulos por la media de su columna.

 **4. Contraste de Hipótesis**
Análisis estadístico para comparar variables entre estaciones y años.

 **5. Algoritmo de Predicción de Estación del año con KNN**
Este algoritmo usa KNN para predecir la estación del año usando los datos meteorológicos.

 **6. Visualización de las fronteras de decisión de la predicción de la estación con KNN**
Visualización de fronteras de decisión de cuando se daría como resultado una estación u otra

 **7. Predicción de la estación del año de manera no Supervisada (K-Means K=6)**
El algoritmo usa la temperatura y humedad con kMeans y 6 clusters para mejorar la precisión
