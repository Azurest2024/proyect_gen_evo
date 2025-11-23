# Proyecto de Análisis de Sedimentos: Metabarcoding de Comunidades Microbianas
## Hipótesis

Se espera que las comunidades microbianas presentes en los sedimentos de diversos ecosistemas acuáticos presenten una composición diferencial según las características ambientales del área, lo que puede estar influenciado por factores como la profundidad, el tipo de sustrato y la exposición a contaminantes. A través del análisis metabarcoding de 16S rRNA, se busca identificar y comparar las comunidades bacterianas presentes en sedimentos de distintas localizaciones, con el fin de entender mejor su relación con los factores ambientales.

## Objetivos

### Objetivo General:
Analizar las comunidades microbianas de sedimentos acuáticos utilizando datos metabarcoding de 16S rRNA, con el fin de explorar la diversidad bacteriana y su relación con las condiciones ambientales de los ecosistemas.

### Objetivos Específicos:

Obtener datos de secuenciación metabarcoding de sedimentos utilizando el protocolo estándar de la literatura.

Procesar los datos utilizando el pipeline BANZAI, optimizando los scripts en Python, R y Bash.

Realizar la asignación taxonómica de las secuencias mediante la base de datos de referencia y evaluar las comunidades bacterianas presentes.

Comparar la diversidad microbiana entre diferentes muestras de sedimentos para identificar posibles patrones ecológicos relacionados con las variables ambientales.

## Dataset

El dataset utilizado en este proyecto proviene de "Frontiers in Microbiology" (Salonen et al., 2021), específicamente de muestras de sedimentos acuáticos. Las secuencias de ADN correspondientes a las muestras fueron obtenidas de varios puntos de sedimento y almacenadas en el repositorio de NCBI bajo el Bioproject PRJNA679187. Las secuencias de 16S rRNA fueron extraídas para ser procesadas y analizadas.

Números de acceso (SRR):

SRR13079473

SRR13079474

SRR13079475

SRR13079476

SRR13079478

SRR13079479

SRR13079480

SRR13079481

## Métodos

Para el análisis, se emplea el pipeline BANZAI obtenido del repositorio del MBARI (https://github.com/MBARI-BOG/BOG-Banzai-Dada2-Pipeline.git) que integra varios lenguajes de programación y herramientas de bioinformática:

Bash: Para la ejecución de los scripts que automatizan el proceso de filtrado y preparación de los datos de secuenciación.

Python: Usado para realizar el procesamiento posterior, como la creación de tablas OTU y análisis adicionales sobre las secuencias.

R: Para análisis estadísticos y visualización de la diversidad microbiana, utilizando herramientas como Dada2 para la denoización y asignación taxonómica.

## Estructura de los Archivos

El repositorio contiene los siguientes archivos y carpetas:

scripts/: Carpeta con los scripts en Bash, R y Python.

Dada2_2019v1.0.r: Script de R para la denoización de secuencias 16S usando Dada2.

Make_otu_taxa_table.py: Script en Python para crear una tabla de OTUs a partir de los resultados de Dada2.

Post_BLAST_processing_dada2_v2.0.sh: Script en Bash para procesar los resultados después de BLAST.

XML_Filter_dada2.py: Filtra los resultados de Dada2 basándose en los parámetros específicos.

dataset/: Carpeta que contiene los archivos de datos de secuenciación (archivos SRA).

## Resultados Esperados

Se espera identificar una alta diversidad bacteriana en las muestras de sedimentos, con diferencias significativas entre las muestras obtenidas de diferentes puntos geográficos. El análisis proporcionará información clave sobre las comunidades microbianas que habitan en los sedimentos acuáticos y cómo su composición se relaciona con las características ambientales locales.
