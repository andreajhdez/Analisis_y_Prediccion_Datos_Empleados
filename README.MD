# Análisis y Predicción de Datos de Empleados

Este proyecto está enfocado en analizar y predecir el comportamiento de los empleados en términos de abandono de la empresa, utilizando técnicas de modelado de datos y Random Forests.

## ¿Cómo Ejecutar Este Proyecto?

Asegúrate de tener instaladas las siguientes bibliotecas de Python:

* pandas
* scikit-learn
* matplotlib
* numpy

Puedes instalar estas dependencias usando pip:

* pip install pandas scikit-learn matplotlib numpy

Pasos para Ejecutar

1. Clonar el Repositorio:
* git clone https://github.com/andreajhdez/Analisis_y_Prediccion_Datos_Empleados
* cd Analisis_y_Prediccion_Datos_Empleados

2. Preparación del Entorno:
Asegúrate de tener Python y pip instalados. Se recomienda usar un entorno virtual para gestionar las dependencias del proyecto.

3. Ejecución del Código:

Ajusta y ejecuta los scripts Python proporcionados para cargar, preprocesar los datos, realizar el análisis exploratorio (EDA), entrenar los modelos de Random Forest y evaluar el rendimiento.

* Asegúrate de ajustar los nombres de los scripts según la estructura de tu proyecto.

4. Interpretación de Resultados:

Analiza las métricas de desempeño (Accuracy, F1 Score) y las matrices de confusión obtenidas para comparar los modelos sin cambios y con class_weight="balanced".

### Breve Resumen del Programa
El análisis realizado incluye:

#### Preprocesamiento de Datos:

Carga de datos desde un archivo CSV.
Verificación y manejo de valores faltantes.
Conversión de variables categóricas y eliminación de registros atípicos.
Imputación de datos faltantes.

#### Análisis Exploratorio de Datos (EDA):

Visualización de la distribución de sexos y niveles de estudio.
Respuesta a preguntas como la propensión de los jóvenes a tomar licencias - se concluye que si se percibe un incremento considerable en la frecuencia de ausencias para las personas menores de 30 años. Por este motivo los jóvenes son más propensos a tomar licencias. 
* El dataset no está balanceado por que como podemos apreciar abajo tenemos unos porcentajes de 20% (en licencia) vs 70% (no en licencia).
En estos casos lo ideal es que cada clase se acerque al 50%

#### Modelado de Datos:

Preparación de datos para el entrenamiento de modelos.
Entrenamiento de dos Random Forests: uno sin cambios y otro con class_weight="balanced".
Evaluación del desempeño de los modelos con métricas como Accuracy, F1 Score y matriz de confusión.

Resultados de los Modelos:

Modelo sin cambios (rf_normal):
Accuracy en entrenamiento: 0.9262
Accuracy en test: 0.8350
F1 Score: 0.8283

Modelo con class_weight="balanced" (rf_balanced):
Accuracy en entrenamiento: 0.9200
Accuracy en test: 0.7985
F1 Score: 0.7972

##### Comparación de Resultados:
El modelo sin cambios (rf_normal) tiene una mayor Accuracy en general, pero puede estar sesgado hacia la clase mayoritaria.
El modelo balanceado (rf_balanced) mejora la capacidad de identificar la clase minoritaria a costa de una precisión global ligeramente menor.
El F1 Score más alto en el modelo sin cambios sugiere una mejor combinación de precisión y recall en general, pero el modelo balanceado mejora el recall de la clase minoritaria.

