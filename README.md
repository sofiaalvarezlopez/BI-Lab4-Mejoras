# Mejoras Laboratorio 4 - Inteligencia de Negocios 
## Sofía Álvarez, Brenda Barahona, Álvaro Plata

Para una descripción detallada de las mejoras, remítase al informe de este laboratorio. A grosso modo, se implementaron dos mejoras: primero, que el modelo funcione sin el campo Unnamed: 0. Segundo, que el modelo responda a valores fuera del rango [0,1] para la variable <code>income_composition_of_resources</code>, lo cual previamente no se realizaba porque no hubo necesidad en el entrenamiento. No obstante, manejar los casos extremos de esta variable es fundamental ya que, de acuerdo con el análisis realizado cuantitativamente, es la de mayor importancia en el modelo (ver carpeta notebook).
De esta forma:
* Una posible estrategia es mejorar el pipeline, en esta forma podríamos tener en cuenta la posibilidad de que no sea agregado la columna “Unnamed: 0”, por lo que, el modelo debería correr exitosamente con o sin esta columna. Creemos que podría mejorarse solamente usando un try-catch, o un condicional, al momento de eliminar las columnas.
* Por otro lado, podríamos dar un mejor manejo a los valores nulos, nosotros los tratamos con la media, pero se podría probar alternativas como la eliminación de estos datos o la imputación con otro valor significativo que no sea la media. En este caso, proponemos dividir todos aquellos valores que sean mayores que 1, entre 1000, para evitar este error.

Para ver las implementaciones de las mejoras y optimizaciones, remítase a los archivos clases.py de notebook y de la carpeta raíz, respectivamente.



