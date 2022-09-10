# TC3006C_portafolio_m2

## Sin Framework

Se entrega una regresión logistica de Orden 1 del dataset de wine.data, del cual la columna de índice se divide en tres para hacer una clasificación binaria en tres columnas llamadas clase1, clase2, y clase 3. En una función se presenta el código utilizado para la clasificación, en donde regresa la función de costo J y los valores de teta.


[0.9332426015596206, 0.15853284994675243]
J test
 -0.9974228749474994
J entrenamiento 
 -1.0101920600625784
theta 
 [0.9332426015596206, 0.15853284994675243]
-------------------------------
[0.9398159665373265, 0.1908884537611282]
J test
 -1.0626024468553315
J entrenamiento 
 -1.076815892814953
theta 
 [0.9398159665373265, 0.1908884537611282]
-------------------------------
[0.9289006618865364, 0.0813355065400378]
J test
 -0.8044844039558522
J entrenamiento 
 -0.7799158472823151
theta 
 [0.9289006618865364, 0.0813355065400378]

### Predicciones

Las predicciones arrojan erroneamente que todas se tratan de la clase 2 cuando se utiliza como variable independiente alcohol, y previamente cuando se estaba usando alcohol, aparecía clase 1.

### Matrices de confusión

Matriz de confusión para train 1
[[ 0  0 80]
 [ 0  0 39]
 [ 0  0  0]]
Matriz de confusión para test 1
[[ 0  0 39]
 [ 0  0 20]
 [ 0  0  0]]
Matriz de confusión para train 2
[[ 0  0 72]
 [ 0  0 47]
 [ 0  0  0]]
Matriz de confusión para test 2
[[ 0  0 35]
 [ 0  0 24]
 [ 0  0  0]]
Matriz de confusión para train 3
[[ 0  0 86]
 [ 0  0 33]
 [ 0  0  0]]
Matriz de confusión para test 3
[[ 0  0 44]
 [ 0  0 15]
 [ 0  0  0]]
 
 ## Con Framework
