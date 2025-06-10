# Análisis de Datos de Alquileres de Airbnb en Nueva York

## Autor
- Nombre: Víctor A. Gutiérrez Martínez
- Contexto: Trabajo de programación para demostrar habilidades en análisis de datos y aprendizaje automático con Python.

## Descripción del Proyecto
Este proyecto consiste en un análisis y limpieza de datos de alquileres de Airbnb en la ciudad de Nueva York, obtenidos del conjunto de datos público de Kaggle (Airbnb Open Data) https://www.kaggle.com/datasets/arianazmoudeh/airbnbopendata/data. El objetivo es demostrar el uso de librerías de Python como Pandas, NumPy y Matplotlib para procesar, limpiar y visualizar datos, además de aplicar técnicas de aprendizaje automático con scikit-learn para estimar precios de alquileres.
El cuaderno TrabajoPython.ipynb incluye pasos para cargar los datos, limpiar valores nulos y tipos inconsistentes, explorar estadísticas descriptivas, visualizar tendencias y entrenar un modelo predictivo para los precios.

## Requisitos
Para ejecutar este cuaderno, necesitarás las siguientes librerías de Python:
pandas: Manipulación y análisis de datos.
numpy: Operaciones numéricas y manejo de arrays.
matplotlib: Visualización de datos (gráficos).
scikit-learn: Modelos de aprendizaje automático (Random Forest).

## Puedes instalarlas ejecutando:
pip install pandas numpy matplotlib scikit-learn

## Estructura del Cuaderno:

### Introducción
Presentación del proyecto y objetivos.
Descripción del conjunto de datos de Airbnb (fuente: Kaggle).

### Carga y Limpieza de Datos
Carga del archivo Airbnb_Open_Data.csv en un DataFrame de Pandas.
Inspección inicial: visualización de columnas, tipos de datos y valores nulos.
Identificación de problemas: tipos mezclados, valores nulos (e.g., columna license con solo 2 valores no nulos).

### Análisis Exploratorio
Estadísticas descriptivas de columnas numéricas (e.g., precio, noches mínimas, reseñas).
Visualización: Gráfico de líneas del precio medio por grupo de vecindarios (neighbourhood group) según el año de construcción, con sombreado para rangos.

### Modelado Predictivo
Preparación de datos: eliminación de columnas irrelevantes, conversión de variables categóricas a dummies.
Entrenamiento de un modelo RandomForestRegressor para predecir precios.
Evaluación: Cálculo de MSE, RMSE y R² (resultados: R² ~ 99.99%).
Predicción de precios para entradas con valores nulos en la columna price.


### Resultados:
Visualización de datos limpios y predichos.
Conclusiones sobre la calidad del modelo y las tendencias observadas.


### Conjunto de Datos 
Fuente: Airbnb Open Data en Kaggle https://www.kaggle.com/datasets/arianazmoudeh/airbnbopendata/data
Columnas Principales:
- id: Identificador del alquiler.
- NAME: Nombre del listado.
- host id, host name: Identificador y nombre del anfitrión.
- neighbourhood group, neighbourhood: Ubicación del alquiler.
- lat, long: Coordenadas geográficas.
- room type: Tipo de habitación (e.g., entera, privada).
- price, service fee: Costos del alquiler.
- minimum nights, number of reviews, reviews per month: Métricas de uso y popularidad.
- construction_year: Año de construcción de la propiedad.
- Otros: availability 365, house_rules, etc.



## Instrucciones de Uso
### Descarga los Datos:
Descarga el archivo Airbnb_Open_Data.csv desde el enlace de Kaggle.
Colócalo en el mismo directorio que el cuaderno TrabajoPython.ipynb.

### Ejecuta el Cuaderno:
Abre TrabajoPython.ipynb en Jupyter Notebook o un entorno compatible (e.g., Google Colab, VS Code).
Asegúrate de tener las librerías instaladas.
Ejecuta las celdas en orden para reproducir el análisis, la limpieza, las visualizaciones y el modelado.

### Notas:
El cuaderno maneja valores nulos y tipos de datos inconsistentes, pero puedes ajustar los pasos de limpieza según tus necesidades.
El modelo Random Forest predice precios con alta precisión (R² ~ 99.99%), pero considera validar con otros enfoques si es necesario.


### Limitaciones
Valores Nulos: Columnas como license tienen datos insuficientes; otras, como last review, tienen muchos valores faltantes.
Tipos Mezclados: Algunas columnas (e.g., price, service fee) requieren limpieza para convertirlas a formatos numéricos.
Rendimiento: El conjunto de datos es grande (102,599 entradas), lo que puede requerir tiempo de procesamiento.

### Licencia
Este proyecto es para fines educativos y de demostración. Los datos provienen de Kaggle y están sujetos a sus términos de uso.
