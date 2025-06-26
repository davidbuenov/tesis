# Recomendación personalizada de documentos en sistemas de recuperación de la información basada en objetivos

**Tesis doctoral presentada por:** D. David Bueno Vallejo [1]

**Para optar al grado de:** Doctor Ingeniero en Informática [1]

**Dirigida por:** Dr. D. Ricardo Conejo Muñoz (Universidad de Málaga) y Dr. D. Amos A. David (Universidad Nancy 2) [1, 2]

**Institución:** Departamento de Lenguajes y Ciencias de la Computación, Universidad de Málaga [1, 2]

**Fecha de presentación/aprobación:** Mayo de 2002 [2] / 25 de marzo de 2003 [3]

[Enlace a página oficial de RIUMA](https://riuma.uma.es/xmlui/handle/10630/39145)

---
## Resumen Audio
Escucha el resumen generado por NotebookLM [aquí](https://davidbuenov.github.io/tesis/ResumenTesisNotebookLM.wav)
## Documento completo 
El pdf final de la tesis doctoral puede descargarse [aquí](https://davidbuenov.github.io/tesis/Tesis%20Doctoral%20David%20Bueno.pdf)
## Referencia
MLA:     Bueno Vallejo, David. Recomendación personalizada de documentos en sistemas de recuperación de la información basada en objetivos. 2003.

APA:     Bueno Vallejo, D. (2003). Recomendación personalizada de documentos en sistemas de recuperación de la información basada en objetivos.

Chicago: Bueno Vallejo, David. «Recomendación personalizada de documentos en sistemas de recuperación de la información basada en objetivos», 2003.

Harvard: Bueno Vallejo, D. (2003) Recomendación personalizada de documentos en sistemas de recuperación de la información basada en objetivos.

Vancouver:  Bueno Vallejo D. Recomendación personalizada de documentos en sistemas de recuperación de la información basada en objetivos. 2003.


 [Teseo](https://www.educacion.gob.es/teseo/imprimirFichaConsulta.do?idFicha=95261)
 [Formato RIS](https://davidbuenov.github.io/tesis/dialnet.ris)
 [Formato BIB](https://davidbuenov.github.io/tesis/dialnet.bib)
## Resumen Ejecutivo

Esta tesis aborda el problema de la sobrecarga de información y la falta de personalización en los sistemas de recuperación de la información (Information Retrieval Systems - IRS), como los motores de búsqueda web [4-7]. Propone una nueva visión de la personalización **orientada a los objetivos del usuario**, a diferencia del refinamiento de consultas tradicional [4, 6, 8]. El trabajo ofrece una arquitectura y los algoritmos necesarios para implementar sistemas IRS que proporcionen respuestas personalizadas en función de las necesidades/objetivos del usuario en cada momento [9]. Se ha comprobado la validez de la propuesta mediante la implementación de un sistema llamado **METIORE** [10-13] que incluye las ideas presentadas y ha sido evaluado en entornos convencionales y web aplicados a bases de datos bibliográficas [10].

## Problema Abordado

Los buscadores web actuales a menudo devuelven cientos o miles de resultados para una consulta, de los cuales el usuario solo examina los primeros 20 o 30 [4, 5]. Aunque la ordenación se basa en la correspondencia con la consulta, no siempre son los documentos más interesantes para el usuario individual [4, 5]. Además, los usuarios no expertos a menudo tienen dificultades para expresar su necesidad de información en el lenguaje de consulta del sistema [4, 5]. La mayoría de los sistemas con personalización suelen tener una visión general de los intereses del usuario con un único modelo, lo que no contempla que un usuario pueda tener diferentes intereses o **objetivos** que no guardan relación entre sí [4, 8, 14, 15]. Esto lleva a recomendaciones irrelevantes en ciertos momentos [6].

## Propuesta Principal: Personalización basada en Objetivos

La tesis propone que la personalización en los sistemas de recuperación de la información se centre en el concepto de **objetivo del usuario** [4, 6, 8, 9, 14, 15]. Un objetivo es la expresión de la necesidad de información del usuario al usar el sistema [16]. Una **sesión** es el tiempo continuo que un usuario utiliza el sistema para satisfacer un objetivo concreto [16]. Al basar la personalización en objetivos, el sistema puede aprender un modelo de usuario específico para cada necesidad o contexto de búsqueda [14, 15]. Esto permite que las recomendaciones y la ordenación de resultados se adapten a lo que el usuario busca *en ese momento* [4, 6, 9, 14, 17].

## Contribuciones Clave

Las principales aportaciones de la tesis incluyen [9, 15, 18, 19]:
*   Un estudio detallado de técnicas de IR y modelado de usuario para comprender las carencias del área [9, 18].
*   Una arquitectura de IR que combina modelos booleanos, vectoriales y probabilísticos, aplicable a distintos tipos de sistemas multimedia y documentales [19].
*   **Algoritmos originales** inspirados en Naïve Bayes para la personalización [15].
*   La visión novedosa de centrar el modelado del usuario alrededor del concepto de **objetivo** [15].
*   La utilización de un **historial inteligente** para que el usuario pueda explotar sus búsquedas y evaluaciones anteriores [19-21].
*   La implementación de un sistema (**METIORE**) para validar la propuesta [10, 19, 22].

## Sistema METIORE

**METIORE (Multimedia coopErative InformaTIOn Retrieval SystEm)** es el prototipo implementado para probar las propuestas teóricas de la tesis [10-13, 23]. Es un entorno que permite implementar sistemas de recuperación de información personalizados con características como [23, 24]:
*   Multi-IRS: Aplicable a prácticamente cualquier base de datos con estructura jerárquica [24].
*   Entrada de datos con **XML**: Permite adaptar bases de datos externas [23, 25].
*   Base de datos Orientada a Objetos: Utiliza listas invertidas y clusters para la gestión eficiente de datos [23, 26, 27].
*   Análisis de datos: Permite realizar búsquedas y análisis complejos sin conocimiento previo de la base de datos [23, 28].
*   Personalización: Reordena resultados de búsqueda y ofrece recomendaciones automáticas basándose en el modelo del usuario y su objetivo actual [23, 29].
*   Cooperación: Ofrece una arquitectura para que los usuarios cooperen a través de Internet [24, 30, 31].
*   Interfaz Multilingüe y Multiplataforma [24].

METIORE puede indexar documentos extrayendo información y utilizando técnicas como la eliminación de "stop words" y el algoritmo de Porter para obtener palabras clave [32, 33].

## Algoritmos Clave: NBM y WNBM

La tesis propone mejoras sobre el algoritmo **Naïve Bayes (NB)** para la recomendación personalizada de objetos [11, 15, 21].
*   **NBM (Naïve Bayes Metiore):** Una modificación de NB diseñada para recomendar objetos (documentos) utilizando modelos de usuario organizados por objetivos [11, 13, 21, 34]. NBM aborda un problema del NB clásico donde la probabilidad conjunta se vuelve cero si un atributo nunca ha aparecido antes, incluso si otros atributos son muy relevantes [34].
*   **WNBM (Weighted Naïve Bayes Metiore):** Una **extensión del algoritmo NBM** [15, 35, 36]. Permite **ponderar la importancia de los distintos parámetros** de un documento (como autor, año, palabras clave) al calcular la probabilidad de interés para el usuario [15, 21, 35, 36]. Esto resuelve el problema de que parámetros con muchos atributos (ej. palabras clave) puedan tener una baja aportación a la evaluación final comparados con parámetros con pocos atributos (ej. año), independientemente de su relevancia real para el usuario [35, 36]. WNBM suma los valores parciales de los parámetros utilizando factores de peso (ωp) que suman 1 [36].

## Validación y Experimentos

La propuesta se validó mediante [10, 22, 37, 38]:
1.  **Comparación con Naïve Bayes:** Se comparó NBM con NB y NBCestnik, mostrando que NBM ordena los documentos de forma similar, pero con la ventaja de ser aplicable a múltiples parámetros y con menor necesidad de cálculo en algunos casos [35, 38, 39]. Los resultados de correlación entre NBM y NBCestnik, por ejemplo, fueron cercanos al 94% [35, 39].
2.  **Experimentos controlados con METIORE (Aplicación):** Pruebas con personal investigador, mostrando que los resultados generados por el algoritmo y la aplicación eran satisfactorios [37, 38]. Se utilizó un sistema de evaluación detallado (correcto, conocido, ?, error) [38, 40]. El uso del historial activo fue considerado interesante por usuarios de varias sesiones [41].
3.  **Experimentos no controlados con METIORE (Web):** Pruebas con usuarios no instruidos a través de una versión web y una base de datos de publicaciones sobre hipermedia adaptativos (AH2002) [37, 38, 41]. A pesar de la falta de instrucción, los usuarios lograron un buen rendimiento [37, 38]. Se utilizó un sistema de evaluación simplificado (interesante, muy interesante, etc.) [38]. Los datos mostraron que los usuarios utilizaron las funciones de búsqueda simple, avanzada, recomendar y consultar historial [42, 43].

## Líneas Futuras

Se plantean como líneas futuras [44]:
*   Aplicación del trabajo para la recomendación de documentos Web, incluyendo la posibilidad de compartir documentos con otros usuarios con objetivos similares [44].
*   Estudiar cómo el historial de otros usuarios con objetivos similares puede ayudar al usuario actual, posiblemente a través de razonamiento basado en casos o correlación de modelos de usuarios [44].

