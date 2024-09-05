# Entrenamiento de un modelo para analizar las terminación de contratos de los clientes de Beta Bank
## Introducción
El banco Beta Bank necesita predecir si un cliente dejará el banco pronto y se tiene los datos sobre el comportamiento pasado de los clientes y la terminación de contratos con el banco.
Se creará un modelo con el máximo valor F1 posible, de al menos 0.59 y se verificará el F1 para el conjunto de prueba. 
Además, se medirá la métrica AUC-ROC para compararla con el valor F1.
## Contenido <a id='back'></a>

* [Introducción](#intro)
* [Carga de liberías y datos](#data_review)
* [Preparación de datos](#seg)
* [Análisis de equilibrio de clases](class)
    * [Parámetro class_weight](#we)
    * [Sobremuestreo](#up)
    * [Submuestreo](#down)
* [¿Qué modelo es mejor?](#train)
    * [Árbol de decisión](#tree)
    * [Bosque aleatorio](#forest)
    * [Regresión logística](#reg)
* [Calidad del modelo](#cal)
* [Conclusión general](#conclusion)
## Conclusion
En conclusión, el mejor modelo para el conjunto de datos fue el bosque aleatorio en el cual se experimentó con los hiperparámetros, min_samples_split y n_estimators, ya que con la evaluación de solo un hiperparametro no se pudo tener el valor F1 deseado. Y la técnica que mejor resultado dio para el equilibrio de clases fue el parámetro class_weight en balanced.
- Los hiperparámetros afectaron la calidad de predidcción.
- Se obtuvo un valor F1 mayor a 0.59 en el conjunto de validación y de prueba.
- El valor AUC-ROC fue mayor a la mitad a 0.5.
