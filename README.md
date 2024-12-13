# Optimización de gastos de marketing
El objetivo de este proyecto es **optimizar los gastos de marketing** de Y.Afisha mediante el análisis de **datos de visitas, pedidos y costos publicitarios**. El estudio busca comprender el **comportamiento del usuario**, identificar **fuentes de adquisición rentables** y calcular métricas clave como el **Costo de Adquisición de Clientes (CAC)**, el **Valor de Vida del Cliente (LTV)** y el **Retorno de la Inversión en Marketing (ROMI)**.

### Herramientas y tipo de proyecto
![Python](https://img.shields.io/badge/python-357ebd?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23357ebd.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23357ebd.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![Seaborn](https://img.shields.io/badge/Seaborn-357ebd?style=for-the-badge)
![NumPy](https://img.shields.io/badge/NumPy-%23357ebd.svg?style=for-the-badge&logo=scipy&logoColor=white)
![Limpieza de datos](https://img.shields.io/badge/Limpieza_de_datos-295F98?style=for-the-badge)
![Transformación de datos](https://img.shields.io/badge/Transformación_de_datos-295F98?style=for-the-badge)
![Análisis de datos](https://img.shields.io/badge/Análisis_de_datos-295F98?style=for-the-badge)
![Análisis de cohortes](https://img.shields.io/badge/Análisis_de_cohortes-295F98?style=for-the-badge)
![Visualización de datos](https://img.shields.io/badge/Visualización_de_datos-295F98?style=for-the-badge)

## Preguntas clave
1. ¿Cuántos usuarios activos diarios, semanales y mensuales tiene la aplicación?
2. ¿Cuáles son las principales fuentes de adquisición de clientes y su rentabilidad?
3. ¿Qué métricas de ventas y conversiones se pueden mejorar?
4. ¿Qué tan efectiva es cada fuente de marketing según su ROMI?

## Metodología
- **Preprocesamiento de datos:** Limpieza de datos (valores ausentes, duplicados, formatos de columnas, y tipos de datos adecuados).
- **Análisis del comportamiento de usuarios** Cálculo de métricas como usuarios activos diarios (DAU), semanales (WAU) y mensuales (MAU), duración de sesiones y frecuencia de retorno.
- **Análisis de ventas:** Evaluación del tamaño promedio de compra, pedidos por cliente y LTV.
- **Pruebas de hipótesis:** Cálculo de CAC, ROMI y costos por fuente de adquisición.

## Conclusiones y recomendaciones

### Comportamiento de usuarios, Ventas y Marketing:
- El 16% de los usuarios regresa semanalmente, pero solo el 4% vuelve mensualmente, indicando una posible necesidad de campañas de retención.
- El tamaño promedio de compra es de $5, con algunos picos en diciembre debido a promociones estacionales. La mayoría de los usuarios realiza un pedido por mes.
- Las fuentes con mayor ROMI es 1, 5 y 9 pues, antes de que las cohortes cumplan el primer mes de edad, el ROMI casi alcanza el 1 en la mayoría de cohortes.
- Destaca la fuente 1 donde, a pesar de ser la segunda fuente en la que menos se gasta, es 3era fuente que más usuarios atrae.

### Recomendaciones:
- Descontinuar las fuentes 7, 9 y 10 debido a su bajo rendimiento.
- Reducir la inversión en la fuente 3, ya que no genera retornos significativos.
- Invertir en la fuente 1, que sigue siendo una aliada clave con baja inversión y alto rendimiento.

## Diccionario de datos
La tabla `visits` (registros del servidor con datos sobre las visitas al sitio web):
- `Uid`: identificador único del usuario;
- `Device`: dispositivo del usuario;
- `Start Ts`: fecha y hora de inicio de la sesión;
- `End Ts`: fecha y hora de término de la sesión;
- `Source Id`: identificador de la fuente de anuncios de la que proviene el usuario.
Todas las fechas de esta tabla están en formato AAAA-MM-DD.

La tabla `orders` (datos sobre pedidos):
- `Uid`: identificador único del usuario que realiza un pedido;
- `Buy Ts`: fecha y hora del pedido;
- `Revenue`: ingresos de Y.Afisha de este pedido.

La tabla `costs` (datos sobre gastos de marketing):
- `source_id`: identificador de la fuente de anuncios
- `dt`: fecha;
- `costs`: gastos en esta fuente de anuncios en este día.
