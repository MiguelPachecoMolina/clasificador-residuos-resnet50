# ♻️ Clasificación Automática de Residuos con Aprendizaje Profundo

## 📝 Descripción del Proyecto
Este proyecto implementa un sistema de visión artificial basado en Aprendizaje Profundo (Deep Learning) diseñado para clasificar automáticamente residuos sólidos y optimizar los procesos de reciclaje. A diferencia de soluciones tradicionales que agrupan los desechos en pocas categorías, este modelo tiene la capacidad de clasificar la basura doméstica en 12 clases distintas, lo que resulta en un incremento significativo en el porcentaje de basura que logra ser reciclada eficientemente.

## 👥 Equipo de Trabajo
Proyecto desarrollado por estudiantes de la Licenciatura en Ciencia de Datos (ESCOM - IPN):
* **Cortes Rosales Israel**
* **Dorado Alcalá Teresa Nathaly**
* **Gallegos Sánchez Celso Alberto**
* **Monteros López José Manuel**
* **Pacheco Molina Miguel Alejandro**
* **Palma Pacheco Alan Daniel**

## 📊 Conjunto de Datos
* **Volumen:** 15,150 imágenes procesadas.
* **Clases (12 categorías):** Papel, cartón, desechos orgánicos, metal, plástico, vidrio verde, vidrio café, vidrio blanco, ropa, zapatos, baterías y basura general.
* **Recopilación:** Las imágenes fueron recolectadas buscando representar escenarios de basura real que simulan el paso por una cinta transportadora de separación.

## ⚙️ Metodología y Tecnologías Aplicadas
* **Extracción de Características (Deep Learning):** Se utilizó Transfer Learning con el modelo preentrenado **ResNet50** (Red Neuronal Convolucional) para extraer los mapas de características visuales de alta dimensionalidad de cada imagen.
* **Clasificación Multiclase:** Se implementó un modelo estadístico de Análisis Discriminante Lineal (**LDA**) sobre las características extraídas para proyectar los datos y maximizar la separabilidad entre las 12 clases.
* **Tecnologías:** Python, PyTorch, Torchvision, Scikit-learn, Matplotlib, PIL.

## 🚀 Despliegue e Inferencia
El repositorio mantiene una arquitectura modular separando el entrenamiento de la inferencia. Cuenta con un script de pruebas independiente (`02_inferencia_y_pruebas.ipynb`) que carga los pesos del extractor de características (`.pth`) y el clasificador (`.joblib`) para evaluar la categoría de nuevas imágenes, arrojando una predicción y su nivel de confianza porcentual en tiempo real.
