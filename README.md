# Procesamiento-de-Imagen

Descripción del Proyecto
En este proyecto implementamos un sistema automatizado de segmentación y conteo de células y patógenos en imágenes de cultivos celulares y tejidos histológicos, utilizando técnicas avanzadas de procesamiento de imágenes y aprendizaje no supervisado. El objetivo principal es desarrollar un método robusto y reproducible que permita la cuantificación precisa de estructuras biológicas de interés clínico y de investigación.

# Objetivos Específicos

- Imagen 1:

Segmentación diferencial de células sanas (núcleos teñidos con hematoxilina) y patógenos (estructuras marrones).
Conteo automatizado para detección precoz de infecciones y evaluación de carga parasitaria.
Posible aplicación clínica: Diagnóstico de enfermedades infecciosas y monitoreo de tratamientos antiparasitarios.

- Imagen 2:

Segmentación de células agrupadas en cultivos o tejidos.
Identificación y conteo de células individuales para la evaluación de viabilidad celular.
Aplicación en investigación: cuantificación de células tras la aplicación de fármacos para analizar toxicidad y respuesta terapéutica.


# Metodología Implementada: Imagen 1

- Preprocesamiento Cromático:

Realce selectivo de hematoxilina mediante transformación CIELAB.
Amplificación de componente b* (azul-amarillo) con factor controlado.
Preservación de información espacial sin introducción de artefactos.


- Segmentación No Supervisada:

Agrupamiento K-Means en espacios de color RGB, HSV y LAB. Escogimos RGB.
Identificación automática de clústeres mediante análisis de centroides.
Asignación contextual basada en características espectrales (B alto = células).


- Cuantificación Automatizada:

Etiquetado conectado de componentes.
Análisis de propiedades con regionprops.
Validación visual con superposición.

# Metodología Implementada: Imagen 2


