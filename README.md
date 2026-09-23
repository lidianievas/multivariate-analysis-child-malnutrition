# 📊 Multivariate Analysis of Child Vulnerability & Malnutrition

Proyecto de **Análisis Estadístico Multivariante** realizado en el **Grado en Matemáticas de la Universidad de Granada**, basado en datos de la encuesta **SMART (2014)** y centrado en el estudio de la vulnerabilidad nutricional infantil en el **Corredor Seco de Guatemala**.

## 📌 Descripción

El objetivo del proyecto fue analizar diferentes factores relacionados con la **desnutrición infantil y el retraso en el crecimiento (stunting)** en niños de 6 a 59 meses, estudiando la relación entre variables antropométricas, socioeconómicas y geográficas.

Para ello, se aplicaron diferentes técnicas de análisis estadístico multivariante para **reducir la dimensionalidad de los datos, identificar perfiles de vulnerabilidad y construir modelos de clasificación**.

## 🔬 Metodología

El análisis se desarrolló íntegramente en **R** y se estructuró en varias etapas:

### 1. Preprocesamiento de datos

* Limpieza y transformación de los datos.
* Integración de diferentes fuentes de información.
* Análisis de datos faltantes e imputación.
* Estandarización de variables.

### 2. Análisis de componentes y factores

Se utilizaron técnicas de reducción de dimensionalidad para estudiar la estructura de las variables:

* **PCA (Principal Component Analysis)**
* **Factor Analysis**
* Test de esfericidad de Bartlett.
* Medida de adecuación muestral KMO.
* Rotación Varimax.

### 3. Análisis de conglomerados

Se aplicó **clustering jerárquico** para identificar grupos de individuos con características similares.

La selección del número de grupos se apoyó en:

* Método de la silueta (*Silhouette Method*).
* Método del codo (*Elbow Method*).
* Dendrogramas.

### 4. Clasificación

Se estudió la capacidad de diferentes modelos de análisis discriminante para clasificar el estado de crecimiento infantil:

* **Linear Discriminant Analysis (LDA)**
* **Quadratic Discriminant Analysis (QDA)**
* División de los datos en conjuntos de entrenamiento y prueba.
* Evaluación del rendimiento sobre datos no utilizados para el entrenamiento.

## 📈 Resultados

Entre los principales resultados del análisis:

* La reducción de dimensionalidad permitió identificar estructuras latentes relacionadas con las características antropométricas y territoriales de la muestra.
* El análisis de conglomerados permitió identificar **dos perfiles diferenciados** dentro de la población estudiada.
* Los modelos discriminantes alcanzaron un **82% de acierto** en la clasificación del estado de *stunting* en el conjunto de evaluación.
* Las variables antropométricas mostraron una relación especialmente relevante con la clasificación del estado nutricional dentro de los modelos analizados.

## 🛠️ Tecnologías y herramientas

**Lenguaje**

* R
* R Markdown

**Análisis estadístico**

* `psych`
* `FactoMineR`
* `factoextra`
* `MASS`
* `biotools`

**Manipulación y visualización**

* `tidyverse`
* `dplyr`
* `ggplot2`
* `corrplot`
* `dendextend`

## 📁 Archivos del proyecto

### 📄 Informe

El informe final con el desarrollo y los resultados del análisis se encuentra en:

👉 [Action_against_hunger.pdf](./Action_against_hunger.pdf)

### 💻 Código

El análisis estadístico completo está desarrollado en **R Markdown**:

👉 [FINAL_CASE_Action_against_hunger.Rmd](./FINAL_CASE_Action_against_hunger.Rmd)

El archivo R Markdown contiene el código utilizado para realizar el preprocesamiento, análisis estadístico, visualización y modelización presentados en el informe.

## 👥 Autores

Proyecto realizado en el marco del **Grado en Matemáticas de la Universidad de Granada** por:

* María Teresa Torres Aguilar
* Margarita Conde Jarava
* Lidia Nievas Dueñas
* Lucía Tejero Jiménez
* María del Pilar Caba Magán

---

**Proyecto académico — Análisis Estadístico Multivariante**


