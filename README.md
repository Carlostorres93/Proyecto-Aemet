Buenas a todos, este es mi primer proyecto basado en Data Science y primero darle las gracias por la oportunidad a Hack a Boss por ofrecerme la forma de poder crecer profesionalmente. 
No podría haber hecho este proyecto sin mis compañeros Pablo Bienert Barberan y Ángel García Domínguez.

Nuestro proyecto se basa en un estudio en la variación de la temperatura a lo largo del tiempo en diferentes ciudades españolas, más concretamente en las estaciones de:
BARCELONA AEROPUERTO; SEVILLA AEROPUERTO; VALENCIA; BILBAO AEROPUERTO; MADRID, RETIRO; OURENSE; HIERRO AEROPUERTO; SALAMANCA AEROPUERTO y PALMA DE MALLORCA, AEROPUERTO

Nuestro proyecto se basa en 4 partes:

1º En la extracción de datos: en este primer paso usamos la API de Aemet para la extracción de todos los datos que queremos para nuestro proyecto.
Para ello usamos las librerías de Requests, time (para aplicar el método sleep) y la librería pprint (para poder reproducir los json).
Primero sacamos nuestra API_KEY de la API de AEMET para poder trabajar por ello. Una vez obtenida la API_KEY, creamos una función del inventario de estaciones para sacar el idema (identificador de las estaciones). 
Posteriormente creamos otra función que sirve para sacar los datos de las estaciones climáticas a través del idema y así obtener todos los datos a través del identificador de las estaciones. Todos estos datos los guardaremos en un.csv para trabajar posteriormente con ello.

2º Transformación de los datos: una vez sacada la tabla completa de todos los datos de todas las estaciones que están en el .csv, importamos dicho .csv y se le aplica un filtro a través de la librería Pandas para obtener los datos que deseamos (Temperaturas, Humedad y Precipitaciones).
Para ello eliminamos las columnas innecesarias con .drop, luego hacemos un .rename para renombrar las columnas y al final creamos un filtrado con df[df["Nombre"].isin(nombres_filtrar)] con las estaciones que queremos.

3º Airtable: Airtable es una plataforma en la cual se puede guardar nuestros trabajos para que varias personas puedan trabajar desde la nube. En esta parte del proyecto creamos una función automática tanto para la carga de los datos como la extracción de los datos.

4º Visualización de los datos: este es el punto más importante ya que es donde se obtiene las conclusiones del proyecto. Para ello usamos diferentes librerías como Folium (para la localización de las estaciones), Seaborn (para la representación grafica de los resultados con Pairplot) y por ultimo Plotly (para la representación grafica interactiva de los resultados y la relación de diferentes parámetros con Heatmap).

La conclusión que sacamos a grandes rasgos con estos datos es que a lo largo del tiempo se aprecia un incremento de la temperatura en diferentes estaciones.

Os dejo en mi repositorio de GitHub, los diferentes archivos que hemos trabajado por si en un futuro alguno de vosotros os puede ayudar con un futuro proyecto. Espero que os haya gustado a todos y espero también que poco a poco haga proyectos más avanzados para que esta comunidad siga creciendo.
