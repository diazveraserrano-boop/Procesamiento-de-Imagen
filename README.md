# Procesamiento de Imágenes celulares

Descripción del Proyecto:<br>
En este proyecto implementamos un sistema automatizado de segmentación y conteo de células y patógenos en imágenes de cultivos celulares y tejidos histológicos, utilizando técnicas avanzadas de procesamiento de imágenes y aprendizaje no supervisado. El objetivo principal es desarrollar un método robusto y reproducible que permita la cuantificación precisa de estructuras biológicas de interés clínico y de investigación.

# Objetivos Específicos

- Imagen 1:

Segmentación diferencial de células sanas (núcleos teñidos con hematoxilina) y patógenos (estructuras marrones).<br>
Conteo automatizado para detección precoz de infecciones y evaluación de carga parasitaria.<br>
Posible aplicación clínica: Diagnóstico de enfermedades infecciosas y monitoreo de tratamientos antiparasitarios.<br>

- Imagen 2:

Segmentación de células agrupadas en cultivos o tejidos.<br>
Identificación y conteo de células individuales para la evaluación de viabilidad celular.<br>
Aplicación en investigación: cuantificación de células tras la aplicación de fármacos para analizar toxicidad y respuesta terapéutica.<br>


# Metodología Implementada: Imagen 1

- Preprocesamiento Cromático:

Realce selectivo de hematoxilina mediante transformación CIELAB.<br>
Amplificación de componente b* (azul-amarillo) con factor controlado.<br>
Preservación de información espacial sin introducción de artefactos.<br>


- Segmentación No Supervisada:

Agrupamiento K-Means en espacios de color RGB, HSV y LAB. Escogimos RGB.<br>
Identificación automática de clústeres mediante análisis de centroides.<br>
Asignación contextual basada en características espectrales (B alto = células).<br>


- Cuantificación Automatizada:

Etiquetado conectado de componentes.<br>
Análisis de propiedades con regionprops.<br>
Validación visual con superposición.<br>

# Metodología Implementada: Imagen 2

- Preprocesamiento:

Cambio de espacio desde RGB a HSV y extracción del canal V.<br>
Aplicación de filtro gaussiano y aumento de contraste.<br>


- Segmentación No Supervisada:

Aplicación de umbralización adaptativa.<br>


- Posprocesamiento y cuantificación automatizada:

Aplicación de método de clausura a la máscara binaria.<br>
Cuantificación mediante labels.<br>
