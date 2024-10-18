# Detección de Enfermedades en Plantas con Modelos de Visión Computacional usando YOLOv10

Este proyecto utiliza **YOLOv10**, un modelo de detección de objetos basado en redes neuronales profundas, para identificar enfermedades en plantas de tomate. El modelo clasifica imágenes de hojas de tomate en categorías como sanas o enfermas, abarcando diferentes tipos de enfermedades comunes en los cultivos.

## Descripción del Proyecto

El proyecto está dividido en varias secciones clave, desde la obtención de datos hasta la implementación y evaluación del modelo. El enfoque principal es optimizar el rendimiento del modelo de detección de enfermedades y aplicar este modelo en escenarios reales, mejorando la detección y monitoreo en tiempo real.

### Enfermedades detectadas
El modelo está entrenado para clasificar las siguientes enfermedades:

- Mancha bacteriana
- Tizón temprano
- Tizón tardío
- Molde de hoja
- Punto objetivo
- Punto negro
- Plantas sanas

## Estructura del Proyecto

1. **Obtención y Preparación de Datos**:
   - **Recopilación de imágenes** de plantas enfermas y sanas.
   - **Preprocesamiento** de los datos, que incluye la limpieza, etiquetado y partición de los conjuntos de entrenamiento y prueba.
   - **Análisis de datos faltantes**: Asegurarse de que el conjunto de datos sea representativo y que no falten datos cruciales.

2. **Entrenamiento del Modelo YOLOv10**:
   - Implementación del modelo **YOLOv10** utilizando las imágenes etiquetadas para detectar enfermedades en las hojas de las plantas.
   - **Ajuste de hiperparámetros** como tasa de aprendizaje, tamaño del lote, y épocas de entrenamiento para maximizar el rendimiento del modelo.
   - Utilización de **técnicas de data augmentation** para aumentar la diversidad del conjunto de datos y mejorar la capacidad de generalización del modelo.

3. **Evaluación del Modelo**:
   - Evaluación del rendimiento del modelo utilizando métricas como la **precisión**, **recall**, **exactitud** y **F1-score**.
   - Análisis de los resultados del modelo y **detección de posibles sesgos** en las predicciones, especialmente en clases menos representadas.

4. **Implementación**:
   - Uso del modelo YOLOv10 en escenarios prácticos para la detección de enfermedades en tiempo real, lo cual permite facilitar el monitoreo en campo de los cultivos.

## Contenido del Notebook (`tomatoe_diseases_detection.ipynb`)

El notebook contiene el flujo completo del proceso, desde la carga y preprocesamiento de los datos hasta la evaluación y visualización de resultados del modelo. A continuación, se detallan las secciones principales:

1. **Importación de librerías**: 
   - Se importan las librerías esenciales como `tensorflow`, `opencv`, `pandas`, `seaborn`, y otras necesarias para el preprocesamiento y entrenamiento del modelo.

2. **Cargar y explorar los datos**:
   - Se cargan los conjuntos de datos de imágenes de hojas de tomate y se realiza una exploración inicial de las imágenes y sus etiquetas correspondientes.
   - Se muestran ejemplos de imágenes etiquetadas de hojas sanas y con enfermedades.

3. **Preprocesamiento de datos**:
   - Limpieza de datos, manejo de valores nulos y normalización de las imágenes.
   - División del conjunto de datos en conjuntos de entrenamiento y prueba.

4. **Configuración del modelo YOLOv10**:
   - Definición de la arquitectura del modelo **YOLOv10**, incluyendo los parámetros clave como los anclajes de las cajas delimitadoras y las capas de salida.
   - Carga de pesos pre-entrenados para transfer learning y ajuste fino del modelo.

5. **Entrenamiento del modelo**:
   - Proceso de entrenamiento del modelo con un conjunto de datos balanceado, utilizando técnicas de aumento de datos y optimización.
   - Monitorización del rendimiento del modelo durante el entrenamiento.

6. **Evaluación del modelo**:
   - Cálculo de métricas de evaluación como **precisión**, **recall**, **F1-score**, y el análisis de la matriz de confusión para evaluar el rendimiento del modelo en las clases de enfermedades.
   - Visualización de los resultados del modelo sobre imágenes de prueba.

7. **Pruebas e Inferencia**:
   - Aplicación del modelo entrenado sobre nuevas imágenes de hojas de tomate para detectar enfermedades.
   - Visualización de las cajas delimitadoras sobre las imágenes y clasificación de las enfermedades detectadas.

## Requisitos

- **Python 3.x**
- Bibliotecas necesarias:
  - `tensorflow`
  - `keras`
  - `opencv-python`
  - `pandas`
  - `seaborn`
  - `matplotlib`
  - `scikit-learn`

Para instalar las dependencias, ejecutar:

```bash
pip install -r requirements.txt
