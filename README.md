# Ibex 35
## _La evolución de sus valores en los últimos 5 años_

![image](https://github.com/javicastano77/IBEX_35-Analysis/assets/156696799/687bb4ae-4850-427d-9dfc-b51d0cbc2ed5)

En la actualidad muchas son las personas que se han aventurado a descubrir el complejo mundo de las inversiones, tratando de averiguar qué palancas se deben activar para tener un retorno elevado en sus activos líquidos. En España, contamos con el Ibex35, un índice de gran reconocimiento, incluso para personas totalmente ajenas al mundo financiero. Este índice está conformado por las 35 empresas que se sitúan en el Top de cada ciclo anual.

Bajo este marco, muchas veces el retorno esperado busca objetivos cortoplacistas, una realidad que se vuelve impracticable si tenemos en cuenta cómo funciona la economía a nivel global y local, y todas aquellas variables exógenas que afectan a la evolución de los valores del mercado. 
Por tanto, el gran interrogante que se plantea es: 

**¿Realmente esas personas han realizado un análisis previo para comprender cómo se mueve el mercado de valores?** De ser así, **¿están aplicando el método correcto para obtener un retorno aceptable?**

> El principal problema del inversor,
> e incluso su peor enemigo,
> es probablemente él mismo.

## 1. Descripción del Proyecto

Los datos del proyecto fueron extraídos de [Yahoo Finance](https://es.finance.yahoo.com/) la sección financiera de Yahoo en donde se pueden buscar [series histórcias](https://es.finance.yahoo.com/quote/IAG.MC/history) de diferentes empresas de todo el mundo. 

En los datos descargados de cada serie temporal podermos encontrar las siguientes variables

* **Date**: día de la serie temporal.
* **Open**: valor de la acción en la apertura del mercado.
* **High**: valor máximo de la acción.
* **Low**: valor mínimo de la acción.
* **Close**: valor de la acción en el cierre del mercado.
* **Adj. Close**: valor de la acción en el cierre, ajustado por divisiones y distribuciones de dividendos o plusvalías.

## 2. Obetivos

El proyecto está dividido en 4 objetivos principales:

1 - Analizar la evolución de los valores del Ibex35 de 2019 a 2024.

3- Desarrollar un modelo para predecir los valores del Ibex35 a futuro.

3-  Implementar un escenario de 2024 para momento óptimo de _trading_.

4- Desarrollar una visualización en Power BI para analizar los puntos anteriores.

## 3. Proceso

Los pasos que han marcado el proyecto son los siguientes:

* i. Extraccion de los datos: descargar la serie temporal para cada empresa.
* ii. Unificación de los datos: consolidar en un único _dataset_ los datos de las 35 empresas.
* iii. Inclusión de nuevas variables: añadir columna de empresa y sector para poder identificar cada serie temporal.
* iv. identificación de la correlación entre variables: identificar qué variables tienen una mayor explicación para predecir la tendencia del precio de la acción.
* v. elección de modelo: testear modelos de regresión para identificar cuál de ellos tiene un error más bajo para cada empresa.
* vi. obtención de predicciones: lanzar el mejor modelo para cada empresa y una vez realizado el entrenamiento, obtener la predicción.
* vii. construcción escenario de rentabilidad: construir diferentes escenarios de inversión con cantidad inicial, haciendo trading en el momento más óptimo.
* viii. comparación de realidad vs predicción: analizar cómo se comportan los datos finales con respecto a la realidad.

## 4. Uso

La información se encuentra recogida en:

| Folder | Link |
| ------ | ------ |
| analysis | [EDA y Visualización](https://github.com/javicastano77/IBEX_35-Analysis/tree/main/analysis) |
| data | [Consolidated e Industries](https://github.com/javicastano77/IBEX_35-Analysis/tree/main/data) |
| documentation | [link](https://github.com/javicastano77/IBEX_35-Analysis/tree/main/documentation) |
| models | [model AR, model OMP](https://github.com/javicastano77/IBEX_35-Analysis/tree/main/models) |
| raw data | [Database, model AR, model OMP](https://github.com/javicastano77/IBEX_35-Analysis/tree/main/data/raw%20data) |

## 5. Conclusiones

Tras la realización del proyecto las principales conclusiones obtenidas son:

1 - La tendencia en los valores de las acciones varía significativamente entre empresa y sector, por lo que se hace necesario estudiar cada una de manera individual.

2 - El testo del modelo de Machine Learning, sin introducir un ajuste (variables exógenas, nº de lgas) se base en utilizar el día anterior como predicción del siguiente día.

3- Los factores externos (inflación, crisis, aconntecimientos internacionales) modifican notablemente los valores de las acciones, dificultando establecer una tendencia estable en un período tan reducido de tiempo.

## 6. Próximos pasos

1 - Introducir variables exógenas para refinar el modelo, como por ejemplo: precio del oro, precio del acero para empresas de construcción, tasa de rentabilidad para el sector bancario, etc.

2 - Realizar pruebas del modelo aumentando o disminuyendo el lag inicial de 5 días para la serie temporal

3- Establecer criterios más precisos para el escenario de trading, como por ejemplo: comprar tras caída consecutiva de 4 días en el valor de una acción.

