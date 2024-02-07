## Videojuegos

![N|Solid](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQwsplkaBkUJyS-zyX0MIY8m2e0W3392zIgIA&usqp=CAU)


Analizar el mercado de videojuegos, con el objetivo de identificar posibles nichos, en donde se pueden desarrollar nuevos productos. 
Encontrar los insights y presentarlos, suponiendo que nuestra audiencia se un grupo inversor dispuesto a invertir en el desarrollo de nuevos productos.

### Preguntas 

* ¿Qué análisis podemos hacer del mercado actual?
* ¿Qué lineamientos generales deberá tener en cuenta el grupo inversor a la hora de determinar el primer juego de la empresa, para lograr aprovechar al máximo las tendencias del mercado, y así lograr el objetivo planteado?
* ¿Qué diferencias encontramos entre las distintas plataformas?
* ¿Qué relación podemos considerar en cuanto a la población e ingresos per cápita de los países? 
* ¿En qué regiones conviene enfocarse?
* ¿Podemos determinar algo con respecto a los rangos etarios u otras características demográficas?
* ¿Podemos estimar las ventas de los juegos actuales o al menos de una categoría? Shooters por ejemplo.

### Recursos
| Archivo
| ------ 
| Indicadores_del_desarrollo_humano_mundial Banco Mundial Indicadores de desarrollo humano. 
| Console_sales Reporte de ventas anuales de consolas. por marca y modelo. 
| Juegos en steam. Reporte con estadísticas de uso de juegos en Steam. Incluye recomendaciones  tiempo de uso, etc. 
| Video Games Sales Reporte de ventas por Video Juego y Plataforma. Incluye ranking y apertura por mercados (NA, EU, Japón y Global). 

------

------

### SOLUCION:

1.- Ingreamos los dos Excels y los dos CSV

2.- en la Tabla Data filtramos y tomamos --> INB per cápita, PPA (a $ internacionales actuales):

* Divide el INB total de un país por su población y lo expresa en dólares internacionales a precios actuales.
  Esta medida indica el ingreso promedio por persona en un país, ajustado por el costo de vida.

3.- Inicio del ETL:
* Identificación de Errores y Problemas: Comenzamos revisando los datos cuidadosamente para identificar cualquier tipo de error o problema potencial. Esto puede incluir:

  * Valores Nulos o Faltantes:
     Buscar valores nulos o faltantes en las columnas de los datos. Los valores nulos pueden afectar la integridad de los cálculos y los análisis, por lo que es importante decidir cómo manejarlos.
  * Valores Incorrectos:
     Examinar los datos en busca de valores incorrectos o incoherentes. Esto podría incluir valores que están fuera del rango esperado, valores que no cumplen con el formato adecuado o valores que contradicen las reglas de negocio.
  * Valores Atípicos (Outliers):
     Identificar valores atípicos o outliers que están significativamente fuera del rango esperado. Los outliers pueden distorsionar el análisis y deben ser examinados cuidadosamente para determinar si son errores de entrada o datos legítimos pero inusuales.
  * Inconsistencias de Datos:
     Buscar inconsistencias entre diferentes conjuntos de datos o dentro del mismo conjunto de datos. Esto podría incluir discrepancias en los formatos de datos, valores que contradicen la lógica del negocio o información contradictoria entre diferentes fuentes.
  * Duplicados de Datos:
     Identificar y elimina duplicados de datos que puedan existir en el conjunto de datos. Los datos duplicados pueden afectar la precisión de los análisis y los informes, por lo que es importante deduplicar los datos antes de la transformación.

4.- Ocultamos las columnas "Series Name", "Series Code","Country Code","2019 [YR2019]"

5.- En la pestaña Transformar seleccionamos la funcion Transponer.

6.- En la misma pestaña seleccionamos la funcion Usar la primera fila como encabezado. 

7.- agregamos una nueva columna año desde el 2000 al 2018 y terminamos con esta tabla.

8.- en el mismo procedimiento continua con el ETL.
