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
 
 El método de aprendizaje utilizado son redes neuronales. Se estudian los puntajes (scores) de las redes neuronales iniciando con 5 capas ocultas hasta 40, lo cual se hace con un ciclo for, que repite este proceso. Debido a que se obtienen los puntajes y matrices de confusión en un solo grupo de for loops, la sección de Obtención de Scores y matrices de confusión tarda un poco para ejecutar.

### Puntajes (scores)

Se hace una visualización del cambio en los puntajes, en donde conforme se cambio el número de capas ocultas y sus unidades (de 5 a 40 con un paso de 5 tanto para las capas como para las unidades), se observa que el puntaje aumenta de casi 40% hasta casi 100% para train, y se presenta algo similar para test.

Se presentan ahora los scores:

#### Para train

[[0.69172932 0.37593985 0.37593985 0.37593985 0.37593985 0.37593985
  0.37593985]
 [0.37593985 0.9924812  0.9924812  0.37593985 0.9924812  0.9924812
  0.9924812 ]
 [0.9924812  0.9924812  0.9924812  0.9924812  0.9924812  0.9924812
  0.37593985]
 [0.9924812  0.9924812  0.9924812  0.9924812  0.37593985 0.9924812
  0.37593985]
 [1.         0.9924812  0.9924812  0.9924812  0.9924812  0.9924812
  0.37593985]
 [0.37593985 1.         0.9924812  0.9924812  0.9924812  0.9924812
  0.9924812 ]]
#### Para test
[[0.75555556 0.46666667 0.46666667 0.46666667 0.46666667 0.46666667
  0.46666667]
 [0.46666667 0.95555556 0.93333333 0.46666667 0.95555556 0.93333333
  0.93333333]
 [0.93333333 0.93333333 0.93333333 0.95555556 0.95555556 0.95555556
  0.46666667]
 [0.93333333 0.93333333 0.93333333 0.93333333 0.46666667 0.93333333
  0.46666667]
 [0.93333333 0.95555556 0.93333333 0.93333333 0.95555556 0.95555556
  0.46666667]
 [0.46666667 0.93333333 0.95555556 0.95555556 0.95555556 0.95555556
  0.95555556]]

### Matrices de confusión

Debido a que son muchas las matrices de confusión (que se encuentran disponibles para verse en el colab), se decidio hacer una visualización del cambio de datos acertados y equivocados conforme aumenta el número de capas ocultas. En este se observa como el número de números acertados por lo general aumenta conforme aumentan (desde 5 a 40 con un paso de 5), y para los errores decresen. Se presentan a continuación los vectores que se describen para esta visualización.

Acertados para train

[ 93,  89,  59,  67,  67,  83,  91,  90, 105,  81,  90,  96, 106,
       107,  99, 107, 100, 121, 120, 129, 129, 122, 121, 121, 121, 122,
       113, 120, 120, 119, 118, 122, 121, 129, 114, 121]
 Acertados para test
 
 [31, 35, 26, 34, 29, 21, 38, 32, 39, 37, 37, 33, 38, 39, 37, 37, 33,
       33, 39, 41, 40, 39, 41, 38, 39, 40, 37, 38, 38, 39, 36, 40, 42, 41,
       42, 42]
  
Incorrectos para train
[40, 44, 74, 66, 66, 50, 42, 43, 28, 52, 43, 37, 27, 26, 34, 26, 33,
       12, 13,  4,  4, 11, 12, 12, 12, 11, 20, 13, 13, 14, 15, 11, 12,  4,
       19, 12]

Incorrectos para test 
[14, 10, 19, 11, 16, 24,  7, 13,  6,  8,  8, 12,  7,  6,  8,  8, 12,
       12,  6,  4,  5,  6,  4,  7,  6,  5,  8,  7,  7,  6,  9,  5,  3,  4,
        3,  3]

 
