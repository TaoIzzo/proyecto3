Documentación del Proyecto: Predicción del Estado Fetal con SVM

Introducción

El objetivo de este proyecto es predecir el estado del feto a partir de un conjunto de 
datos médicos utilizando modelos de machine learning. El dataset contiene 2016 
registros con diversas variables relacionadas con la salud del feto, y nuestro objetivo es 
predecir el estado fetal como la variable objetivo. A continuación, se describen las 
variables utilizadas:

• Id: Identificador único del feto.
• b: Hora inicial.
• e: Hora final.
• LBE: Frecuencia cardiaca del feto.
• AC: Número de aceleraciones por segundo.
• FM: Número de movimientos fetales por segundo.
• UC: Número de contracciones uterinas por segundo.
• ASTV: Porcentaje de tiempo con variabilidad anormal a corto plazo.
• MSTV: Valor medio de la variabilidad a corto plazo.
• ALTV: Porcentaje de tiempo con variabilidad anormal a largo plazo.
• MLTV: Valor medio de la variabilidad a largo plazo.
• DL: Número de desaceleraciones leves por segundo.
• DS: Número de desaceleraciones severas por segundo.
• DP: Número de desaceleraciones prolongadas por segundo.
• DR: Número de desaceleraciones repetitivas por segundo.
• Anchura: Anchura del histograma de la frecuencia cardiaca fetal (FHR).
• Min: Valor mínimo (baja frecuencia) del histograma de la frecuencia cardiaca 
fetal (FCF).
• Max: Valor máximo (alta frecuencia) del histograma de la FCF.
• Nmax: Número de picos del histograma.
• Nzeros: Número de ceros del histograma.
• Mode: Moda del histograma.
• Mean: Media del histograma.
• Median: Mediana del histograma.
• Variance: Varianza del histograma.
• Tendency: Tendencia del histograma.
• Target: Código de clase del estado fetal.

Para la creación del modelo, los datos se dividieron en conjuntos de entrenamiento y 
prueba, con una proporción del 60% y 40%, respectivamente, garantizando la 
diversidad de los datos y evitando sesgos.
Algoritmo SVM (Support Vector Machine)
El modelo de Support Vector Machine (SVM) fue elegido como uno de los principales 
algoritmos debido a su capacidad para trabajar con problemas de clasificación 
complejos y su robustez frente a los outliers. Para optimizar el rendimiento del modelo, 
se realizó una búsqueda en cuadrícula (Grid Search) de hiperparámetros con el fin de 
encontrar la mejor combinación posible:

Resultados del SVM

Los mejores hiperparámetros obtenidos fueron:
• C: 1
• Kernel: linear
El modelo final obtuvo una precisión del 96% en el conjunto de prueba y una precisión 
del 97% en el conjunto de entrenamiento, lo cual indica un buen rendimiento general 
sin sobreajuste significativo. Estos resultados muestran que el modelo SVM es capaz 
de capturar las características relevantes para la clasificación del estado fetal.

Análisis de Resultados

El modelo SVM con kernel lineal se destacó entre los modelos probados, mostrando la 
mejor capacidad predictiva y estabilidad. La elección del kernel lineal permite una 
interpretación más sencilla y eficiente del modelo, sin requerir transformaciones 
complejas de los datos. Además, la búsqueda de hiperparámetros ayudó a optimizar el 
rendimiento, evitando el sobreajuste.

En comparación con otros modelos como Naive Bayes Gaussiano y Multinomial, el 
modelo SVM con kernel lineal obtuvo una mejor precisión en el conjunto de prueba, lo 
cual indica una mayor capacidad para generalizar y hacer predicciones correctas sobre 
datos no vistos.

Conclusión

El modelo SVM con kernel lineal demostró ser el mejor enfoque para predecir el estado 
fetal con los datos disponibles, alcanzando una precisión del 96% en el conjunto de 
prueba. Este rendimiento superior, combinado con la simplicidad del kernel lineal, lo 
convierte en una excelente opción para la clasificación del estado de salud del feto. La 
optimización de hiperparámetros fue fundamental para g
