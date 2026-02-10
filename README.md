# ConnectaTel – Análisis de Clientes y Patrones de Uso

## Objetivo del Proyecto 

Este proyecto tiene como propósito analizar el comportamiento de los clientes de ConnectaTel integrando información demográfica y datos de uso del servicio (llamadas y mensajes). Para ello se desarrolló un flujo completo de análisis que incluye:

* Integración y depuración de bases provenientes de distintas fuentes, asegurando consistencia en tipos de datos, formatos y valores.
* Validación y estandarización de la información para detectar registros incompletos, inconsistentes o atípicos.
* Construcción de perfiles estadísticos que describen el uso del servicio por cliente y por segmentos demográficos.
* Identificación de outliers y patrones atípicos, utilizando métodos estadísticos y visualizaciones para entender comportamientos fuera de lo esperado.
* Segmentación de clientes basada en edad, país y nivel de uso, con el fin de comparar grupos y detectar diferencias relevantes.
* Extracción de insights accionables que puedan apoyar decisiones comerciales y de producto.

## Datasets Utilizados

* plans.csv: Catálogo de planes con sus precios y beneficios.
* users_latam.csv: Información de cada usuario (datos personales, plan, fecha de registro, churn).
* usage.csv: Actividad generada por los usuarios: llamadas, mensajes, duración, longitud.

## Etapas del análisis 

1. Cargar y explorar
  - Cargar y explorar plans, users_latam, usage.
  - Visión clara de la estructura y tipos de columna de cada dataset. 
2. Identificación de problemas de calidad
  - Contar nulos, detectar sentinels, revisar fechas fuera de rango.
  - Lista priorizada de problemas que pueden sesgar decisiones.
3. Limpieza básica
  - Reemplazar sentinels, convertir fechas, imputar o marcar NA según reglas.
  - Datos consistentes y listos para análisis estadístico.   
4. Summary statistics
  - Revisar las medidas clave en variables categóricas y numéricas.
  - Medidas clave (media, mediana, percentiles) que muestran el comportamiento típico y extremo
5. Visualización & outliers
  - Creación de histogramas y boxplots.
  - Visualización de sesgos, patrones de usuarios o datos atípicos.    
6. Segmentación
  - Crear segmentaciones basadas en reglas claras; visualizar proporciones con countplots.
  - Segmentos accionables que permiten diseñar ofertas, campañas y migraciones de plan.     
7. Insight ejecutivo
  - Redactar conclusiones y recomendaciones comerciales basadas en los pasos anteriores.
  - Responder a las preguntas del negocio y proponer acciones concretas.  
8. Publicación
  - Subir tu notebook + README a GitHub.
  - Entrega reproducible para revisión y ejecución por stakeholders.

## Principales Hallazgos

* La mayoría de los clientes se concentra en el segmento de uso medio
* Existe un grupo pequeño pero importante de usuarios de alto uso, que representan una oportunidad para planes premium o ilimitados
* Los adultos son el grupo etario más numeroso, mientras que los adultos mayores también representan un segmento relevante
* Se detectaron usuarios con consumos muy altos de minutos, lo que sugiere potencial para planes especializados o corporativos

##Recomendaciones de Negocio

* Diseñar planes diferenciados para clientes de alto uso (más minutos y beneficios exclusivos)
* Crear estrategias de retención para clientes de uso medio, incentivando su migración a planes superiores
* Analizar campañas específicas para adultos mayores, que muestran presencia relevante en la base
* Usar segmentaciones tipo ABC–XYZ combinando valor del cliente y estabilidad de consumo

## Cómo ejecutar el notebook

1. Abre el archivo .ipynb en Google Colab o Jupyter Notebook
2. Ejecuta las celdas en orden
3. Asegúrate de tener instaladas las librerías: pandas
      - numpy
      - matplotlib
      - seaborn
