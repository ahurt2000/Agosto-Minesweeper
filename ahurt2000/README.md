Minesweeper
===========

Idea
----

* Each cell mined notifies its neighbors.* Cada celda notifica a sus vecinas al ser minada.
La solución se desarrolla en dos clases, una Field (Campo de minas) compuesto por sus Cell(celdas, escaques, cuadros) 

Cada celda:

-devuelve sus vecinos teniendo en cuenta el tamaño del campo al que pertenencen. 
-se imprime segun su estado minado * el valor de su peligrosidad (danger) o Cero.

Cada campo:

-se genera segun dimensiones
-se imprime segun lo especificado, e imprime sus celdas
-puede minar una de sus celdas(consecuentemente las celdas vecinas cambian su estado de peligro)

Para el procesamiento de las entradas del ejercicio planteado se creo una clase Excercise capaz de:

-Recibir las entradas descritas (ver Readme del ejercicio varios campos se crean desde la entrada) 
-crear y procesar los campos de la entrada
-obtener la salida descrita


tests:
------

Se crearon los test para las clases ver folder test (para ejecutar los test necesitas PHPUnit)

##El test CellTest

- Comprueba que se devuelva correctamente las celdas vecinas (Each cell is able to return their neighboring cells)
- se realizan 9 test, el método getNeighbor() debe devuelver los vecinos adecuados para los casos extremos que se prueban
- Se contruye la clase *Cell* y se obtiene

*CellTest-->**ok** *

##El test para los Campos (FieldTest)

- Cada campo generado debe ser resuelto con las salidas ideadas en los test 
- Se crea la clase *Field* de forma que el método printField() nos devuelva la salida esperada en la prueba.

*FieldTest---**ok** *


## El test del ejercicio (ExerciseTest)

- Esta prueba se alimenta con el la entrada propuesta en el mismo ejerccio y la salida que se espera.
- Se crea una clase *Exercise* capaz de procesar la entrada y generar la salida para adecuada, 
  instanciando la Clase Field

*ExerciseTest---**ok** *

Salida
------

Se agrega un index.php para mostrar un hipotético uso de la clase Exercise, con entra desde array,
Salidas de Exercise con la entrada del Readme propuesto en el ejercicio

# php -f index.php

