# Manipular-DM-Data 

Partiendo de una trayectoria de dinámica molecular de una membrana modelo podemos usar
`up_or_down.py` para seleccionar la monocapa que queremos analizar. Esta función devuelve un
AtomGroup (MDAnalysis).

Podemos usar lo que devuelva la función `up_or_down` para generar un archivo .csv, ya sea con la
función `cartesian_to_polar` o `acomodar_data` que devuelven un archivo.csv con las columnas siendo
la selección (residuo, átomo, etc) que hayamos seleccionado. Es decir, si selección = átomoP,
entonces columnas serán átomoP_1, átomoP_2,..., átomoP_N y los renglones son los frames de la
simulación. El valor de cada celda en este arreglo depende de la función que usemos.

Podemos usar dicho arreglo para calcular la matriz de correlación de Pearson, tal que podamos
gráficar los resultados usando un mapa de calor. Usando lo que devuelva la función
(`cartesian_to_polar` o `acomodar_data`) podemos utilizar `normalized_pears_corr` para gráficar un
mapa de valor sólo con los puntos significativos.
