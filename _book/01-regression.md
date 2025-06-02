# 🔍 **1. Regressión** {-}

**Ejemplos:** Linear Regression, Ridge, Lasso   
**Cuándo usarlo:**

* Predicción de valores numéricos continuos (e.g. precios, temperaturas).  
* Relaciones lineales entre variables. 

**Ventajas:** Simple, interpretable.   
**Limitaciones:** Mal desempeño con relaciones no lineales complejas.

## Ordinary Least Squares Regression (`OLSR`) {-} 

**Regresión de Mínimos Cuadrados Ordinarios (OLSR)**: un método de regresión lineal para estimar los parámetros desconocidos mediante la creación de un modelo que minimizará la suma de los errores cuadrados entre los datos observados y los predichos (valores observados y valores estimados).  

## Linear Regression {-} 

**Regresión lineal** : se utiliza para estimar valores reales (costo de las casas, número de visitas, ventas totales, etc.) basados en variables continuas.

## Logistic Regression {-} 

**Regresión logística** : se utiliza para estimar valores discretos (valores binarios como 0/1, sí/no, verdadero/falso) basados en un conjunto dado de variables independientes.

## Stepwise Regression {-} 

**Regresión por pasos** : añade características al modelo una a una hasta encontrar la puntuación óptima para tu conjunto de características. La selección por pasos alterna entre el avance y el retroceso, incorporando y eliminando variables que cumplen los criterios de entrada o eliminación, hasta alcanzar un conjunto estable de variables.  

## Multivariate Adaptive Regression Splines (`MARS`) {-} 

**Splines de Regresión Adaptativa Multivariante (`MARS`)**: un método de regresión flexible que busca interacciones y relaciones no lineales que ayudan a maximizar la precisión predictiva. Este algoritmo es inherentemente no lineal (lo que significa que no es necesario adaptar el modelo a patrones no lineales en el datos agregando manualmente términos del modelo (squared terms, interaction effects).   

## Locally Estimated Scatterplot Smoothing (`LOESS`) {-} 

**Locally Estimated Scatterplot Smoothing (`LOESS`)**: un método para ajustar una curva suave entre dos variables o una superficie  entre un resultado y hasta cuatro variables predictoras. La idea es que, si los datos no se distribuyen linealmente, se puede aplicar el concepto de regresión. Se puede aplicar regresión, lo que se denomina regresión ponderada localmente. Se puede aplicar LOESS cuando la relación entre las variables independientes y dependientes no es lineal. Hoy en día, la mayoría de los algoritmos (como las redes neuronales de propagación hacia adelante clásicas, las máquinas de vectores de soporte, los algoritmos del vecino más cercano, etc.) son sistemas de aprendizaje global que se utilizan para minimizar las funciones de pérdida globales (por ejemplo, el error cuadrático medio). Por el contrario, los sistemas de aprendizaje local dividen el problema de aprendizaje global en múltiples problemas de aprendizaje más pequeños y simples. Esto generalmente se logra dividiendo la función de costo en múltiples funciones de costo locales independientes. Una de las desventajas de los métodos globales es que, a veces, ningún valor de parámetro puede proporcionar una aproximación suficientemente buena. Pero entonces surge LOESS, una alternativa a la aproximación de funciones globales.   


## Regression Ridge {-} 

**Regresión Ridge** es una extensión de la regresión lineal clásica (`OLS`) que se usa cuando hay problemas de multicolinealidad o riesgo de sobreajuste. Aborda estos problemas introduciendo un término de penalización a la función de coste de la regresión lineal ordinaria (mínimos cuadrados ordinarios, OLS).  

## Least Absolute Shrinkage and Selection Operator (`LASSO`) {-}

**Least Absolute Shrinkage and Selection Operator (`LASSO`)**: es otra técnica de regularización utilizada en modelos de regresión lineal, similar a la Regresión Ridge, pero con una diferencia clave en el tipo de penalización que aplica en la función de coste de la regresión lineal ordinaria.    


---
