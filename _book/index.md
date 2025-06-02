--- 
title: "Machine Learning (Apuntes) "
author: "Diana Villasana Ocampo"
date: "2025-06-02"
site: bookdown::bookdown_site
documentclass: book
bibliography: [book.bib, packages.bib]
# url: your book url like https://bookdown.org/yihui/bookdown
# cover-image: path to the social sharing image like images/cover.jpg
description: |
  This is a minimal example of using the bookdown package to write a book.
  The HTML output format for this example is bookdown::bs4_book,
  set in the _output.yml file.
biblio-style: apalike
csl: chicago-fullnote-bibliography.csl
---

# Machine Learning {-}

## 🔍 **1. Regressión** {-}

**Ejemplos:** Linear Regression, Ridge, Lasso   
**Cuándo usarlo:**

* Predicción de valores numéricos continuos (e.g. precios, temperaturas).  
* Relaciones lineales entre variables. 

**Ventajas:** Simple, interpretable.   
**Limitaciones:** Mal desempeño con relaciones no lineales complejas.

### Ordinary Least Squares Regression (`OLSR`) {-} 

**Regresión de Mínimos Cuadrados Ordinarios (OLSR)**: un método de regresión lineal para estimar los parámetros desconocidos mediante la creación de un modelo que minimizará la suma de los errores cuadrados entre los datos observados y los predichos (valores observados y valores estimados).  

### Linear Regression {-} 

**Regresión lineal** : se utiliza para estimar valores reales (costo de las casas, número de visitas, ventas totales, etc.) basados en variables continuas.

### Logistic Regression {-} 

**Regresión logística** : se utiliza para estimar valores discretos (valores binarios como 0/1, sí/no, verdadero/falso) basados en un conjunto dado de variables independientes.

### Stepwise Regression {-} 

**Regresión por pasos** : añade características al modelo una a una hasta encontrar la puntuación óptima para tu conjunto de características. La selección por pasos alterna entre el avance y el retroceso, incorporando y eliminando variables que cumplen los criterios de entrada o eliminación, hasta alcanzar un conjunto estable de variables.  

### Multivariate Adaptive Regression Splines (`MARS`) {-} 

**Splines de Regresión Adaptativa Multivariante (`MARS`)**: un método de regresión flexible que busca interacciones y relaciones no lineales que ayudan a maximizar la precisión predictiva. Este algoritmo es inherentemente no lineal (lo que significa que no es necesario adaptar el modelo a patrones no lineales en el datos agregando manualmente términos del modelo (squared terms, interaction effects).   

### Locally Estimated Scatterplot Smoothing (`LOESS`) {-} 

**Locally Estimated Scatterplot Smoothing (`LOESS`)**: un método para ajustar una curva suave entre dos variables o una superficie  entre un resultado y hasta cuatro variables predictoras. La idea es que, si los datos no se distribuyen linealmente, se puede aplicar el concepto de regresión. Se puede aplicar regresión, lo que se denomina regresión ponderada localmente. Se puede aplicar LOESS cuando la relación entre las variables independientes y dependientes no es lineal. Hoy en día, la mayoría de los algoritmos (como las redes neuronales de propagación hacia adelante clásicas, las máquinas de vectores de soporte, los algoritmos del vecino más cercano, etc.) son sistemas de aprendizaje global que se utilizan para minimizar las funciones de pérdida globales (por ejemplo, el error cuadrático medio). Por el contrario, los sistemas de aprendizaje local dividen el problema de aprendizaje global en múltiples problemas de aprendizaje más pequeños y simples. Esto generalmente se logra dividiendo la función de costo en múltiples funciones de costo locales independientes. Una de las desventajas de los métodos globales es que, a veces, ningún valor de parámetro puede proporcionar una aproximación suficientemente buena. Pero entonces surge LOESS, una alternativa a la aproximación de funciones globales.   


### Regression Ridge {-} 

**Regresión Ridge** es una extensión de la regresión lineal clásica (`OLS`) que se usa cuando hay problemas de multicolinealidad o riesgo de sobreajuste. Aborda estos problemas introduciendo un término de penalización a la función de coste de la regresión lineal ordinaria (mínimos cuadrados ordinarios, OLS).  

### Least Absolute Shrinkage and Selection Operator (`LASSO`) {-}

**Least Absolute Shrinkage and Selection Operator (`LASSO`)**: es otra técnica de regularización utilizada en modelos de regresión lineal, similar a la Regresión Ridge, pero con una diferencia clave en el tipo de penalización que aplica en la función de coste de la regresión lineal ordinaria.    


---

## 🌲 **2. Árboles de Decisión y Derivados** {-}  

**Ejemplos:** Decision Tree, Random Forest, Gradient Boosting  
**Cuándo usarlo:**  

* Problemas tabulares con relaciones no lineales y variables categóricas o numéricas.
* Cuando interpretabilidad es importante.

**Ventajas:** Manejan datos heterogéneos, fáciles de interpretar (árboles simples).   
**Limitaciones:** Sobreajuste en árboles simples; menor desempeño en datos muy ruidosos sin ensambles.

---

## 🌟 **3. Ensambles (Ensemble Methods)** {-}

**Ejemplos:** Random Forest, AdaBoost, XGBoost, LightGBM   
**Cuándo usarlo:**   

* Cuando buscas alto rendimiento en clasificación o regresión tabular.
* Competencias de datos (como Kaggle).

**Ventajas:** Alta precisión, robustez.   
**Limitaciones:** Difícil de interpretar; más costosos computacionalmente.

---

## 🧠 **4. Redes Neuronales y Deep Learning** {-}  

**Ejemplos:** MLP, CNN, RNN, Transformers   
**Cuándo usarlo:**   

* Imágenes (CNN), texto y lenguaje natural (Transformers), series temporales (RNN/LSTM).
* Grandes volúmenes de datos no estructurados.

**Ventajas:** Muy poderosos para datos complejos y no estructurados.   
**Limitaciones:** Requieren mucha data y poder computacional. Menor interpretabilidad.

---

## 🧩 **5. Reducción de Dimensionalidad** {-}   

**Ejemplos:** PCA, t-SNE, UMAP   
**Cuándo usarlo:**   

* Visualización de datos de alta dimensión.
* Preprocesamiento para eliminar ruido o multicolinealidad.

**Ventajas:** Mejora desempeño y velocidad de otros modelos.    
**Limitaciones:** Puede perder interpretabilidad; no siempre mejora modelos.

---

## 🧬 **6. Bayesianos** {-}  

**Ejemplos:** Naive Bayes, Bayesian Networks  
**Cuándo usarlo:**   

* Clasificación rápida con supuestos simples.
* Problemas de texto o spam detection.

**Ventajas:** Muy rápidos, bien fundamentados.   
**Limitaciones:** Supone independencia de variables (no siempre cierto).

---

## 🧮 **7. Regularización** {-}  

**Ejemplos:** L1 (Lasso), L2 (Ridge), Elastic Net   
**Cuándo usarlo:**   

* Para evitar sobreajuste en modelos lineales o redes neuronales.
* Cuando tienes muchas variables (alta dimensionalidad).

**Ventajas:** Penaliza modelos complejos.   
**Limitaciones:** Puede eliminar variables útiles si se usa en exceso.

---

## 🔍 **8. Instance-Based (Basados en Instancias)** {-}  

**Ejemplos:** K-Nearest Neighbors (KNN)   
**Cuándo usarlo:**   

* Pocos datos, con patrones locales claros.  
* Cuando la similitud entre casos es importante.

**Ventajas:** Simple y eficaz en problemas de baja dimensión.   
**Limitaciones:** Escala mal con muchos datos; sensible al ruido.

---

## 📏 **9. Clustering (No Supervisado)** {-}  

**Ejemplos:** K-Means, DBSCAN, Hierarchical Clustering  
**Cuándo usarlo:**   

* Agrupar datos sin etiquetas previas.
* Descubrir estructuras ocultas o segmentos de mercado.

**Ventajas:** Útil en exploración y reducción de complejidad.   
**Limitaciones:** Requiere elegir número de grupos (excepto DBSCAN); puede ser sensible a escala.

---

## 📐 **10. Sistemas Basados en Reglas (Rule-Based Systems)** {-}

**Ejemplos:** RuleFit, Decision Rules, lógica difusa
**Cuándo usarlo:**

* Interpretabilidad es clave (por ejemplo, decisiones legales o médicas).
* Incorporar conocimiento experto.

**Ventajas:** Fácil de entender y auditar.   
**Limitaciones:** No tan precisos como otros métodos en datos complejos.

---

## 📌 Cuadro


```{=html}
<div id="vrbbrtxmbb" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
  
  <table class="gt_table" style="-webkit-font-smoothing: antialiased; -moz-osx-font-smoothing: grayscale; font-family: 'Century Gothic'; display: table; border-collapse: collapse; line-height: normal; margin-left: auto; margin-right: auto; color: #333333; font-size: 10px; font-weight: normal; font-style: normal; background-color: #FFFFFF; border-top-style: solid; border-top-width: 2px; border-top-color: #A8A8A8; border-right-style: none; border-right-width: 2px; border-right-color: #D3D3D3; border-bottom-style: solid; border-bottom-width: 2px; border-bottom-color: #A8A8A8; border-left-style: none; border-left-width: 2px; border-left-color: #D3D3D3; table-layout: fixed; width: 0px;" data-quarto-disable-processing="false" data-quarto-bootstrap="false" width="0" bgcolor="#FFFFFF">
  <colgroup>
    <col style="width:200px;">
    <col style="width:200px;">
    <col style="width:200px;">
    <col style="width:300px;">
  </colgroup>
  <thead style="border-style: none;">
    <tr class="gt_heading" style="border-style: none; background-color: #FFFFFF; text-align: center; border-bottom-color: #FFFFFF; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3;" bgcolor="#FFFFFF" align="center">
      <td colspan="4" class="gt_heading gt_title gt_font_normal gt_bottom_border" style="border-style: none; color: #333333; font-size: 14px; padding-top: 4px; padding-bottom: 4px; padding-left: 5px; padding-right: 5px; background-color: #FFFFFF; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; border-bottom-style: solid; border-bottom-width: 2px; border-bottom-color: #D3D3D3; text-align: left; font-weight: bold;" align="left" bgcolor="#FFFFFF">Modelos y cuando usarlos</td>
    </tr>
    
    <tr class="gt_col_headings" style="border-style: none; border-top-style: solid; border-top-width: 2px; border-top-color: #D3D3D3; border-bottom-style: solid; border-bottom-width: 2px; border-bottom-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3;">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="Tipo" style="border-style: none; color: #333333; background-color: #FFFFFF; font-size: 100%; font-weight: normal; text-transform: inherit; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: bottom; padding-top: 5px; padding-bottom: 6px; padding-left: 5px; padding-right: 5px; overflow-x: hidden; text-align: left;" bgcolor="#FFFFFF" valign="bottom" align="left">Tipo</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="Problema_tipico" style="border-style: none; color: #333333; background-color: #FFFFFF; font-size: 100%; font-weight: normal; text-transform: inherit; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: bottom; padding-top: 5px; padding-bottom: 6px; padding-left: 5px; padding-right: 5px; overflow-x: hidden; text-align: left;" bgcolor="#FFFFFF" valign="bottom" align="left">Problema_tipico</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="Ventajas" style="border-style: none; color: #333333; background-color: #FFFFFF; font-size: 100%; font-weight: normal; text-transform: inherit; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: bottom; padding-top: 5px; padding-bottom: 6px; padding-left: 5px; padding-right: 5px; overflow-x: hidden; text-align: left;" bgcolor="#FFFFFF" valign="bottom" align="left">Ventajas</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="Cuando_usarlo" style="border-style: none; color: #333333; background-color: #FFFFFF; font-size: 100%; font-weight: normal; text-transform: inherit; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: bottom; padding-top: 5px; padding-bottom: 6px; padding-left: 5px; padding-right: 5px; overflow-x: hidden; text-align: left;" bgcolor="#FFFFFF" valign="bottom" align="left">Cuando_usarlo</th>
    </tr>
  </thead>
  <tbody class="gt_table_body" style="border-style: none; border-top-style: solid; border-top-width: 2px; border-top-color: #D3D3D3; border-bottom-style: solid; border-bottom-width: 2px; border-bottom-color: #D3D3D3;">
    <tr style="border-style: none;"><td headers="Tipo" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Regressión</td>
<td headers="Problema_tipico" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Valores numéricos</td>
<td headers="Ventajas" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Simplicidad</td>
<td headers="Cuando_usarlo" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Relaciones lineales</td></tr>
    <tr style="border-style: none;"><td headers="Tipo" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Árboles / Decision Tree</td>
<td headers="Problema_tipico" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Clasificación, regresión</td>
<td headers="Ventajas" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Interpretabilidad</td>
<td headers="Cuando_usarlo" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Datos tabulares</td></tr>
    <tr style="border-style: none;"><td headers="Tipo" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Ensambles</td>
<td headers="Problema_tipico" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Clasificación, regresión</td>
<td headers="Ventajas" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Precisión</td>
<td headers="Cuando_usarlo" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Alto rendimiento, Kaggle</td></tr>
    <tr style="border-style: none;"><td headers="Tipo" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Deep Learning</td>
<td headers="Problema_tipico" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Imágenes, texto, audio</td>
<td headers="Ventajas" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Modelos complejos</td>
<td headers="Cuando_usarlo" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Datos grandes y no estructurados</td></tr>
    <tr style="border-style: none;"><td headers="Tipo" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Reducción de Dim.</td>
<td headers="Problema_tipico" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Visualización, preprocesamiento</td>
<td headers="Ventajas" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Mejora eficiencia</td>
<td headers="Cuando_usarlo" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Datos con muchas variables</td></tr>
    <tr style="border-style: none;"><td headers="Tipo" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Bayesianos</td>
<td headers="Problema_tipico" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Clasificación rápida</td>
<td headers="Ventajas" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Velocidad</td>
<td headers="Cuando_usarlo" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Texto, spam detection</td></tr>
    <tr style="border-style: none;"><td headers="Tipo" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Regularización</td>
<td headers="Problema_tipico" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Evitar overfitting</td>
<td headers="Ventajas" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Generalización</td>
<td headers="Cuando_usarlo" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Modelos lineales con muchas variables</td></tr>
    <tr style="border-style: none;"><td headers="Tipo" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Instance-Based</td>
<td headers="Problema_tipico" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Clasificación</td>
<td headers="Ventajas" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Simple, no requiere entrenamiento</td>
<td headers="Cuando_usarlo" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Pocos datos y relaciones claras</td></tr>
    <tr style="border-style: none;"><td headers="Tipo" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Clustering</td>
<td headers="Problema_tipico" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Agrupamiento no supervisado</td>
<td headers="Ventajas" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Descubrir estructuras ocultas</td>
<td headers="Cuando_usarlo" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Segmentación sin etiquetas</td></tr>
    <tr style="border-style: none;"><td headers="Tipo" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Rule-Based</td>
<td headers="Problema_tipico" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Interpretabilidad</td>
<td headers="Ventajas" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Lógica clara</td>
<td headers="Cuando_usarlo" class="gt_row gt_left" style="border-style: none; padding-top: 1px; padding-bottom: 1px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Reglas conocidas, decisiones explicables</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes" style="border-style: none; color: #333333; background-color: #FFFFFF; border-bottom-style: none; border-bottom-width: 2px; border-bottom-color: #D3D3D3; border-left-style: none; border-left-width: 2px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 2px; border-right-color: #D3D3D3;" bgcolor="#FFFFFF">
    <tr style="border-style: none;">
      <td class="gt_footnote" colspan="4" style="border-style: none; margin: 0px; font-size: 90%; padding-top: 4px; padding-bottom: 4px; padding-left: 5px; padding-right: 5px;"> Fuente: Elaboración propia</td>
    </tr>
  </tfoot>
</table>
</div>
```





