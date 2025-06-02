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

# url: your book url like https://bookdown.org/yihui/bookdown

Placeholder


## 📌 Cuadro

<!--chapter:end:index.Rmd-->


# 🔍 **1. Regressión** {-}

Placeholder


## Ordinary Least Squares Regression (`OLSR`) {-} 
## Linear Regression {-} 
## Logistic Regression {-} 
## Stepwise Regression {-} 
## Multivariate Adaptive Regression Splines (`MARS`) {-} 
## Locally Estimated Scatterplot Smoothing (`LOESS`) {-} 
## Regression Ridge {-} 
## Least Absolute Shrinkage and Selection Operator (`LASSO`) {-}

<!--chapter:end:01-regression.Rmd-->

# 🌲 **2. Árboles de Decisión y Derivados** {-}  

**Ejemplos:** Decision Tree, Random Forest, Gradient Boosting  
**Cuándo usarlo:**  

* Problemas tabulares con relaciones no lineales y variables categóricas o numéricas.
* Cuando interpretabilidad es importante.

**Ventajas:** Manejan datos heterogéneos, fáciles de interpretar (árboles simples).   
**Limitaciones:** Sobreajuste en árboles simples; menor desempeño en datos muy ruidosos sin ensambles.

---

<!--chapter:end:02-decision_tree.Rmd-->

# 🌟 **3. Ensambles (Ensemble Methods)** {-}

**Ejemplos:** Random Forest, AdaBoost, XGBoost, LightGBM   
**Cuándo usarlo:**   

* Cuando buscas alto rendimiento en clasificación o regresión tabular.
* Competencias de datos (como Kaggle).

**Ventajas:** Alta precisión, robustez.   
**Limitaciones:** Difícil de interpretar; más costosos computacionalmente.

---

<!--chapter:end:03-ensemble.Rmd-->

# 🧠 **4. Redes Neuronales y Deep Learning** {-}  

**Ejemplos:** MLP, CNN, RNN, Transformers   
**Cuándo usarlo:**   

* Imágenes (CNN), texto y lenguaje natural (Transformers), series temporales (RNN/LSTM).
* Grandes volúmenes de datos no estructurados.

**Ventajas:** Muy poderosos para datos complejos y no estructurados.   
**Limitaciones:** Requieren mucha data y poder computacional. Menor interpretabilidad.

---

<!--chapter:end:04-neural-networks.Rmd-->

# 🧩 **5. Reducción de Dimensionalidad** {-}   

**Ejemplos:** PCA, t-SNE, UMAP   
**Cuándo usarlo:**   

* Visualización de datos de alta dimensión.
* Preprocesamiento para eliminar ruido o multicolinealidad.

**Ventajas:** Mejora desempeño y velocidad de otros modelos.    
**Limitaciones:** Puede perder interpretabilidad; no siempre mejora modelos.

---

<!--chapter:end:05-dimensionality_reduction.Rmd-->

# 🧬 **6. Bayesianos** {-}  

**Ejemplos:** Naive Bayes, Bayesian Networks  
**Cuándo usarlo:**   

* Clasificación rápida con supuestos simples.
* Problemas de texto o spam detection.

**Ventajas:** Muy rápidos, bien fundamentados.   
**Limitaciones:** Supone independencia de variables (no siempre cierto).

---

<!--chapter:end:06-bayesian.Rmd-->

# 🧮 **7. Regularización** {-}  

**Ejemplos:** L1 (Lasso), L2 (Ridge), Elastic Net   
**Cuándo usarlo:**   

* Para evitar sobreajuste en modelos lineales o redes neuronales.
* Cuando tienes muchas variables (alta dimensionalidad).

**Ventajas:** Penaliza modelos complejos.   
**Limitaciones:** Puede eliminar variables útiles si se usa en exceso.

---

<!--chapter:end:07-regularization.Rmd-->

# 🔍 **8. Instance-Based (Basados en Instancias)** {-}  

**Ejemplos:** K-Nearest Neighbors (KNN)   
**Cuándo usarlo:**   

* Pocos datos, con patrones locales claros.  
* Cuando la similitud entre casos es importante.

**Ventajas:** Simple y eficaz en problemas de baja dimensión.   
**Limitaciones:** Escala mal con muchos datos; sensible al ruido.

---

<!--chapter:end:08-instance_based.Rmd-->

# 📏 **9. Clustering (No Supervisado)** {-}  

**Ejemplos:** K-Means, DBSCAN, Hierarchical Clustering  
**Cuándo usarlo:**   

* Agrupar datos sin etiquetas previas.
* Descubrir estructuras ocultas o segmentos de mercado.

**Ventajas:** Útil en exploración y reducción de complejidad.   
**Limitaciones:** Requiere elegir número de grupos (excepto DBSCAN); puede ser sensible a escala.

---

<!--chapter:end:09-clustering.Rmd-->

# 📐 **10. Sistemas Basados en Reglas (Rule-Based Systems)** {-}

**Ejemplos:** RuleFit, Decision Rules, lógica difusa
**Cuándo usarlo:**

* Interpretabilidad es clave (por ejemplo, decisiones legales o médicas).
* Incorporar conocimiento experto.

**Ventajas:** Fácil de entender y auditar.   
**Limitaciones:** No tan precisos como otros métodos en datos complejos.

---

<!--chapter:end:10-rule_based_systems.Rmd-->


# References {-}


Sagi, S. (2019). ML Algorithms: One SD (σ). The obvious questions to ask when… | by Sagi Shaier | Medium. https://medium.com/@Shaier/ml-algorithms-one-sd-%CF%83-74bcb28fafb6 

Kuhn, M. (2019). The caret Package. https://topepo.github.io/caret/index.html

<!--chapter:end:11-references.Rmd-->

