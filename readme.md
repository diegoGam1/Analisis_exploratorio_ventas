# ANÁLISIS EXPLORATORIO DE DATOS (EDA)
## [DIEGO GAMARRA]


## Contienido
- src/ -> Contiene un archivo jupyter notebook llamado "Analisis.ipynb" con el analisis exploratorio, la carpeta data y la carpeta visualizacion
- data/ -> contiene tres archivos csv:
    - Sales "Data.csv" -> Es nuestro set de datos inicial con datos de ventas
    - "Sales_Data_Final" -> Es nuestro set de datos final luego del analisis exploratorio
    - "rules.csv" -> Contiene los datos sobre el market basket analysis, nos dice qué productos se compran juntos.
- visualizacion/ -> Contiene el archivo "Dashboard_ventas.pbix" con el storytelling y dashboard
- requirements.txt -> contiene las librerias necesarias para el proyecto

## Cómo usar
- 1 Clona el repositorio
    - git clone https://github.com/diegoGam1/Proyecto_Final_Makeit.git
- 2  Instala las dependencias
    - pip install -r requirements.txt


# Resumen del proyecto

##  Descripción del proyecto


    Este proyecto de analisis exploratorio de datos (EDA) busca extraer información clave sobre las ventas y rentabilidad de productos, así como identificar patrones de compra en un dataset de transacciones para optimizar el manejo de inventarios y mejorar las estrategias de marketing para aumentar las ventas. La finalidad es proporcionar insights que puedan ayudar en la toma de decisiones estratégicas basadas en datos.



##  Objetivos especificos

1. Identificar los productos más vendidos y aquellos con menor rendimiento en términos de ventas.
2. Determinar los productos que generan más ingresos y cuáles tienen el menor margen de rentabilidad.
3. Analizar la distribución de ingresos por estado, identificando en qué regiones los productos más rentables tienen mejor o peor desempeño.
4. Descubrir combinaciones de productos que los clientes compran juntos con frecuencia.
5. Proponer estrategias basadas en las asociaciones de compra identificadas.

## Datos Utilizados

El dataset contiene información sobre transacciones de productos realizadas en diferentes estados de EE.UU. con las siguientes variables principales:

- Customer_id	= Id de cada cliente
- Order ID = Id único de cada orden de compra
- Product = Nombre del producto 
- Quantity Ordered = Cantidad del producto 
- Price Each = Precio unitario
- Order Date = Fecha del pedido
- Purchase Address = Direccion de la compra
- Month	= Mes de la compra
- Day = dia de la compra
- Sales = Total de la compra
- Season = Estación del año de la compra
- City = ciudad de la compra
- State = estado de la compra
- Hour = Hora de la compra

##  Metodología del Análisis

###  Carga y Exploración Inicial

- Se cargaron los datos y se realizó un análisis estadístico básico.
- Se detectaron valores atípicos pero no fueron tratados, ya que corresponden a precios unitarios, totales y unidades. No consideramos que sean datos extremos o errones, solamente es la naturaleza de los datos y si los imputaramos o modificaramos serían datos incorrectos. 
- Se decidió omitir el análisis temporal ya que los datos abarcan solo un año y nuestro enfoque es hacia los productos.

### Análisis Univariado

- Se analizaron las distribuciones de cada variable para comprender su comportamiento.
- Se identificaron los productos más vendidos y los que tienen un menor desempeño.

###  Análisis Multivariado

- Se realizaron gráficos comparativos entre la cantidad de unidades vendidas por producto y los ingresos generados.
- Se analizaron los productos más rentables en cada estado.
- Se generaron gráficos de Pareto para visualizar las ventas e ingresos por producto.

###  Patrones de compra
- Se realizo un market basket analysis
- Se utilizó el modelo apriori para detectar patrones de compra conjunta.
- Se identificaron los productos que se venden juntos con mayor frecuencia.

## Conclusiones y Hallazgos Clave

- **Productos más vendidos**: Se identificaron los productos con mayor demanda y aquellos con menor desempeño.
- **Productos más rentables**: Algunos productos generan altos ingresos a pesar de no ser los más vendidos.
- **Distribución por estados**: Se encontraron diferencias en la rentabilidad de productos según la región.
- **Patrones de compra**: Se detectaron combinaciones de productos que suelen comprarse juntos, lo que puede ser útil para estrategias de venta cruzada y promociones.

##  Recomendaciones Estratégicas

- 1. Optimizar inventarios asegurando suficiente stock de los productos más vendidos en las regiones con mayor demanda.
- 2. Ajustar estrategias de precios y promociones para los productos con menor rentabilidad.
- 3. Implementar ofertas y paquetes de productos combinados basados en el análisis de compras conjuntas.
- 4. Personalizar estrategias de marketing según los patrones de consumo en cada estado.
 
