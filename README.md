📊 Multivariate Analysis of Child Vulnerability & Malnutrition | Action Against Hunger (Guatemala)

Este repositorio contiene el trabajo final de análisis estadístico multivariante desarrollado en la Universidad de Granada (UGR), centrado en la caracterización de la desnutrición infantil y la vulnerabilidad sociodemográfica en el Corredor Seco de Guatemala a partir de datos de la encuesta estandarizada SMART (2014).

📌 Contexto del Proyecto

En 2014, el Corredor Seco guatemalteco enfrentó una severa crisis humanitaria derivada de una sequía prolongada (45 días) y la plaga de la roya del café (La Roya). Estos eventos agotaron las reservas básicas de grano y mermaron la oferta de mano de obra agrícola en comunidades rurales.

El objetivo central del estudio fue evaluar e identificar qué variables explican y predicen con mayor precisión la vulnerabilidad nutricional y el retraso en el crecimiento (stunting) en niños de 6 a 59 meses, contrastando el peso predictivo de indicadores biométricos frente a variables socioeconómicas y geográficas.

🔬 Metodología y Técnicas Estadísticas

El análisis se llevó a cabo íntegramente en R, cubriendo las siguientes etapas y métodos multivariantes:

Preprocesamiento y Limpieza de Datos:

Consolidación y fusión de bases de datos ($N = 704$ menores).

Análisis de homogeneidad en datos faltantes ($p > 0.05$) e imputación.

Normalización de variables continuas (Z-scores).

Reducción de la Dimensionalidad:

PCA (Principal Component Analysis): Verificación de supuestos con test de esfericidad de Bartlett y KMO ($\text{MSA} = 0.75$). Retención de 3 componentes principales explicando el 86% de la varianza total acumulada.

FA (Factor Analysis): Estimación por residuos mínimos (minres) y rotación ortogonal Varimax. Estructura óptima de 3 factores latentes explicando el 75.1% de la varianza:

Factor 1: Desarrollo físico integral (WEIGHT, HEIGHT, MONTHS).

Factor 2: Dimensión geográfica/territorial (ESTRATO.x).

Factor 3: Balance y proporcionalidad nutricional aguda (MUAC - circunferencia braquial media).

Segmentación de la Población:

Cluster Analysis (Hierarchical Clustering): Determinación del número óptimo de agrupaciones mediante el coeficiente de silueta (Silhouette Method), método del codo (Elbow Method / WSS) y dendrograma jerárquico.

Se validaron 2 perfiles claros de vulnerabilidad:

Cluster 1 (Alto Riesgo Biológico): Medias estandarizadas negativas en peso (-0.83), talla (-0.83), edad (-0.85) y MUAC (-0.52).

Cluster 2 (Mayor Estabilidad Biológica/Económica): Valores superiores al promedio muestral en todas las métricas biométricas e ingresos.

Clasificación y Validación Predictiva:

Discriminant Analysis (LDA & QDA): Variable dependiente STUNTING (retraso en el crecimiento).

Evaluación de supuestos de normalidad multivariante (Shapiro-Wilk) y test M de Box ($p < 9.84 \times 10^{-16}$), justificando el uso de fronteras cuadráticas (QDA).

Validación cruzada con partición 80% entrenamiento / 20% prueba.

Tasa de acierto / Precisión: 82% de clasificación correcta.

💡 Principales Conclusiones

Primacía Biométrica: A pesar de que la ubicación geográfica y la economía familiar definen el entorno estructural, la identificación efectiva del stunting depende de forma casi exclusiva de variables antropométricas (peso y talla, seguidas de MUAC).

Inconsistencia de Predictores Socioeconómicos: Indicadores como el número de fuentes de ingresos (NUM_FUENT_INGRES) o el estrato presentaron solapamiento y bajo poder de discriminación directa sobre el estado nutricional agudo/crónico.

Implicación en Políticas de Ayuda: Las estrategias de triaje y focalización de fondos de emergencia deben priorizar el monitoreo antropométrico sistemático en centros de salud comunitarios por encima de los censos meramente económicos.

📁 Estructura del Repositorio

├── data/
│   └── raw/                  # Datos brutos de la encuesta SMART (si aplica)
│   └── processed/            # Dataset limpio tras imputación (N=704)
├── scripts/
│   ├── 01_data_cleaning.R    # Limpieza, homogeneidad e imputación
│   ├── 02_pca_fa.R           # Análisis de componentes principales y factorial
│   ├── 03_cluster_analysis.R # Clustering jerárquico, métricas de corte
│   └── 04_discriminant.R     # Modelado LDA / QDA y mapas de partición
├── reports/
│   └── Action_against_hunger.pdf  # Informe técnico final
└── README.md


🛠️ Paquetes de R Utilizados

Análisis Multivariante: psych, FactoMineR, factoextra, MASS, biotools

Visualización: ggplot2, corrplot, dendextend

Manipulación de Datos: tidyverse, dplyr

👥 Autores

Trabajo realizado en el marco de la Universidad de Granada (UGR) por:

María Teresa Torres Aguilar

Margarita Conde Jarava

Lidia Nievas Dueñas

Lucía Tejero Jiménez

María del Pilar Caba Magán
