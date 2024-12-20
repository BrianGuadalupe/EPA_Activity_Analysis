# EPA_Activity_Analysis
Este proyecto consiste en el análisis de datos de la Encuesta de Población Activa (EPA), un conjunto de microdatos proporcionados por el Instituto Nacional de Estadística (INE). Los objetivos principales incluyen la exploración, el preprocesamiento, el análisis predictivo y la creación de modelos de aprendizaje supervisado para abordar diversas preguntas relacionadas con las características demográficas, educativas y laborales de los individuos.

## Objetivos del Proyecto
### Regresión logística sobre la actividad laboral:
Predicción de si una persona realizó un trabajo remunerado (variable TRAREM) en función de características como género (SEXO1), edad (EDADNum), estado civil (ECIV1), nacionalidad (NAC1), nivel de formación (NFORMA) y edad de finalización de estudios (EDADEST). Evaluación del modelo mediante métricas como la matriz de confusión, la curva ROC y el área bajo la curva (AUC). 

### Regresión sobre la antigüedad laboral (DCOM):
Análisis de los datos del 1º, 2º y 3º trimestre de 2023 para predecir la antigüedad en la empresa en días.
Uso de árboles de regresión, bosques aleatorios y boosting para el modelado, con evaluación del error cuadrático medio (MSE).

### Análisis discriminante lineal y cuadrático:
Clasificación de los individuos según su actividad económica principal (AOI) usando características demográficas y educativas.
Validación cruzada y comparación de modelos lineales y cuadráticos con métricas como precisión y matrices de confusión.

### Predicción de la actividad principal (ACT1):
Uso de los datos del 1º, 2º y 3º trimestre de 2024 para entrenar un modelo de Random Forest que predice la actividad principal (ACT1) del 4º trimestre de 2024.
Identificación de variables importantes y evaluación mediante la matriz de confusión y precisión.

### Exploración de distribuciones y relaciones:
Visualización de distribuciones mediante diagramas de cajas y gráficos de dispersión para analizar variables como número de publicaciones (Num_Publicaciones), reacciones (Num_Reacciones) y antigüedad laboral.

## Estructura del Proyecto
- data/: Contiene los microdatos originales y los procesados (no incluidos en el repositorio por confidencialidad).
- scripts/: Scripts de análisis en R, organizados por objetivo:
- logistic_regression.R: Regresión logística para TRAREM.
- regression_dcom.R: Modelado predictivo de la antigüedad laboral.
- discriminant_analysis.R: Análisis discriminante para AOI.
- random_forest_ACT1.R: Predicción de la actividad principal (ACT1).
- results/: Gráficos, tablas y métricas generadas durante el análisis.
- README.md: Descripción general del proyecto.
- .gitignore: Archivos y carpetas ignorados por Git.

## Técnicas y Herramientas Usadas
- Lenguaje: R.
- Librerías:
dplyr, tidyr: Manipulación de datos.
ggplot2: Visualización de datos.
randomForest: Bosques aleatorios.
mice: Imputación de valores faltantes.
rpart: Árboles de regresión.
xgboost: Boosting.
- Modelos de Aprendizaje Supervisado:
Regresión logística, árboles de decisión, bosques aleatorios, boosting y análisis discriminante.

## Resultados Clave
### Regresión logística (TRAREM):
El modelo mostró una AUC de 0.78, indicando una capacidad predictiva moderada. La edad (EDADNum) y el nivel educativo (NFORMA) fueron variables altamente significativas.

### Antigüedad laboral (DCOM):
El modelo de boosting presentó el menor MSE comparado con árboles y bosques aleatorios.

### Análisis discriminante (AOI):
El análisis discriminante cuadrático superó al lineal en precisión, especialmente para clases con baja representación.

### Actividad principal (ACT1):
El modelo de Random Forest tuvo una precisión del 82%, destacando la relevancia de las variables EDADNum y NFORMA
