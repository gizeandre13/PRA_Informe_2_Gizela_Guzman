# Evaluación del impacto del balanceo de clases en la segmentación semántica urbana con SegNet en imágenes aéreas de alta resolución

Este repositorio contiene los notebooks utilizados para entrenar y evaluar cuatro configuraciones de un modelo de segmentación semántica aplicado a cartografía urbana. El estudio se realizó sobre la zona urbana del municipio de Santa Rosa de Osos (Antioquia, Colombia), empleando ortoimágenes de alta resolución y datos vectoriales oficiales capturados mediante restitución fotogramétrica 3D.

Cada configuración implementa combinaciones de balanceo de clases, pesos en la función de pérdida, normalización y distintas número de épocas, con el objetivo de evaluar el impacto en el desempeño de las clases minoritarias y en la estabilidad del entrenamiento.

## 📁 Conjunto de datos

El conjunto de datos utilizado para el entrenamiento y evaluación se construyó a partir de los productos cartográficos oficiales generados para Santa Rosa de Osos:

**Ortoimágenes de alta resolución**: 
- Resolución espacial de 10 cm
- División en mosaicos de 2000 × 2000 píxeles
- Cada mosaico se utiliza como entrada del modelo en formato RGB

**ISPRS Vaihingen**: ortofotos **IRRG** (9 cm GSD)

Clases (ISPRS):  
🛣️ **Carreteras**
🏠 **Edificios**
🌱 **Vegetación baja**
🌳 **Árboles**
🚗 **Carros**
❓ **Desorden**

Link de descarga: [https://www.isprs.org/resources/datasets/benchmarks/UrbanSemLab/Default.aspx]

## 💻 Notebook

Notebook Jupyter con el código fuente del proyecto, que inculye la carga de datos, preprocesamiento, entrenamiento SegNet, evaluación y generación de resultados.

## ⚙️ Utilidades

Este notebook requiere algunas bibliotecas útiles, como `torch`, `scikit-image`, `numpy` y `matplotlib`. Las cuales se instalalan por medio de pip install -r requirements.txt.

Se adjunta archivo de texto que contiene la lista de librerías necesarias junto con sus versiones compatibles, optimizadas para Python 3.10.0.

## 🧠 Modelo

Se adjunta el archivo .pt del modelo SegNet entrenado sobre el dataset ISPRS Vaihingen, listo para inferencia y evaluación.

## 📝 Documentos

Se incluye un reporte en formato de artículo que describe la implementación, entrenamiento y evaluación de la arquitectura SegNet.

## 🗺️ Resultados 

Se incluyen cuatro mosaicos resultantes del proceso de inferencia realizado con el modelo entrenado sobre la arquitectura SegNet.


## 🙌 Créditos

- Código basado en **SegNet** y cuadernos de **DeepNetsForEO**.
  [https://github.com/nshaud/DeepNetsForEO/tree/master]
- Implementación de la linea base presentada en:
  ["Más allá de RGB: teledetección urbana de muy alta resolución con redes profundas multimodales "](https://hal.archives-ouvertes.fr/hal-01636145),
  *Nicolas Audebert*, *Bertrand Le Saux* y *Sébastien Lefèvre*, ISPRS Journal, 2018.
  
