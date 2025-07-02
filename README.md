
## Ajuste de modelos bi-lineales con punto de quiebre no pre-establecido

**Modelos lineal plató o meseta**

**Modelo con Plató en la Izquierda**

En muchos fenómenos biológicos, el uso de modelos lineales con quiebre resulta una simplificación muy útil de la relación entre variables. Por ejemplo, se sabe que el rendimiento de soja disminuye al atrasar la fecha de siembra; sin embargo, esta disminución no es lineal, sino que el atraso de la fecha de siembra no parece afectar demasiado al rinde en un principio, pero a partir de un momento dado las pérdidas siguen una tendencia lineal. En este caso, determinar el punto a partir del cual los rindes empiezan a ser afectados así como conocer a qué tasa estos rindes van decreciendo una vez superado dicho punto de inflexión, son preguntas de alto interés agronómico.
En la figura Nº 1 se presenta un conjunto de datos simulados describiendo esta situación.  

<p align="center">
  <img src="imagenes/Fig.1.JPG" alt="Figura 1" width="500">
</p>

Figura 1: Rendimientos máximos de un cultivar de soja y la fecha de siembra expresada como días desde una fecha base.

En esta situación hay tres parámetros a estimar
**dc**  día en el que se produce el quiebre de la tendencia
**A**= nivel medio de rendimiento antes del día dc
**p**= pérdida de rendimiento por día a partir del día dc. 

El modelo teórico que se propone para describir esta relación es:

<p align="center">
  <img src="imagenes/ECUACION.1.jpg" alt="Figura 1" width="500">
</p>

El modelo de la Ec. Nº 1, es un modelo no lineal en los parámetros pues en algunos de sus términos a parece la multiplicación de algunos de ellos.
Por lo tanto la función que utilizaremos para ajustar este modelo es “nls” del paquete “stats” de R, que realiza una ajuste de mínimos cuadrados de un modelo no lineal.

