# sprint7_final_project_telecom_analysis
ConnectaTel Telecom Analysis – Proyecto 6
Este repositorio contiene el análisis realizado durante el Proyecto 6 del curso, correspondiente al caso de ConnectaTel, una empresa de telecomunicaciones con operaciones en México y Colombia.

El análisis integra tres datasets (plans.csv, users_latam.csv, usage.csv) que simulan datos reales de usuarios, planes y consumo de servicios móviles (llamadas y mensajes), con el objetivo de identificar patrones de uso, detectar comportamientos atípicos y comprender qué segmentos de clientes muestran necesidades diferenciadas.

📂 Contenido del repositorio
notebooks/connectatel_analysis.ipynb → Notebook principal con limpieza, EDA, análisis de distribuciones, detección de outliers, segmentación de clientes y conclusiones ejecutivas.

data/plans.csv → Catálogo de planes con precios, minutos incluidos, GB incluidos y costos por excedente.

data/users_latam.csv → Información de clientes: edad, ciudad, fecha de registro, plan contratado y churn.

data/usage.csv → Detalle de uso real: llamadas (duración) y mensajes (longitud) por usuario.

README.md → Este archivo.

🧠 Objetivo del análisis
Identificar problemas de calidad de datos (valores nulos, sentinels, fechas fuera de rango, valores inválidos)

Construir un pipeline de limpieza reproducible

Analizar distribuciones de edad, mensajes, llamadas y minutos por tipo de plan

Detectar outliers en variables clave de uso

Segmentar clientes por nivel de uso (Bajo, Medio, Alto) y por edad (Joven, Adulto, Adulto Mayor)

Generar insights y recomendaciones comerciales para el equipo de ConnectaTel

📊 Etapas del análisis realizadas
Carga y exploración inicial → Carga de los tres datasets y revisión de estructura, tipos de datos y primeras filas.

Identificación de problemas de calidad → Detección de valores nulos, sentinels, fechas fuera de rango y valores inválidos.

Limpieza básica → Reemplazo de sentinels, conversión de fechas, imputación de valores nulos y marcado de fechas futuras como NA.

Summary statistics → Resumen estadístico de variables numéricas y categóricas.

Visualización y outliers → Histogramas y boxplots para identificar distribuciones y valores extremos.

Segmentación → Creación de segmentos por nivel de uso (Bajo, Medio, Alto) y por edad (Joven, Adulto, Adulto Mayor).

Insight ejecutivo → Conclusiones y recomendaciones comerciales basadas en los hallazgos.

📈 Principales hallazgos
Calidad de datos: Se detectaron y corrigieron valores ausentes en city (14.1%), fechas futuras en reg_date (40 registros en 2026) y valores atípicos en age (-999 reemplazados por la mediana).

Distribución de uso: Los usuarios del plan Premium muestran mayor volumen de mensajes y llamadas en comparación con el plan Básico.

Segmentación por edad: Los usuarios de 40-60 años prefieren mayoritariamente el plan Básico, mientras que los mayores de 70 años muestran preferencia por el plan Premium.

Outliers: Se identificaron 46 usuarios con más de 11.5 mensajes, 30 con más de 10.5 llamadas y 109 con más de 61.9 minutos (menos del 3% del total). Se decidió mantenerlos por su bajo porcentaje y valor comercial potencial.

Segmentos: El 37.5% de los usuarios son de Bajo uso, el 45% de Uso medio y el 17.5% de Alto uso.

💡 Recomendaciones comerciales
Revisar el plan Básico: Dado que concentra al 64.9% de los usuarios, especialmente jóvenes y adultos de bajo uso, se podría considerar un plan más económico con menos beneficios para atraer a usuarios ocasionales.

Fortalecer el plan Premium: Los usuarios de mayor edad y alto uso muestran preferencia por este plan. Agregar beneficios adicionales como minutos o mensajes ilimitados para fidelizar a este segmento.

Crear un plan intermedio: El segmento de Uso medio (45% de los usuarios) representa una oportunidad para lanzar un plan con beneficios intermedios.

Segmentación por edad: Diseñar campañas específicas para Jóvenes, Adultos y Adultos Mayores.

Monitoreo de outliers: Los usuarios con consumo extremo deben ser analizados individualmente como potenciales clientes de alto valor.

▶ Cómo abrir el notebook en Google Colab
Haz clic en el siguiente botón:

https://colab.research.google.com/assets/colab-badge.svg

O:

Abre el archivo sprint7_final_project_telecom_analysis.ipynb en GitHub

Haz clic en Open in Colab

📘 Cómo reproducir el análisis
Opción 1: En Google Colab (recomendado)

Abre el notebook en Google Colab

Ejecuta la primera celda que contiene:

python
from google.colab import files
uploaded = files.upload()
Selecciona los archivos plans.csv, users_latam.csv y usage.csv desde tu computador

Ejecuta todas las celdas en orden

Opción 2: En Jupyter Notebook local

Clona este repositorio

Asegúrate de tener los archivos CSV en la carpeta data/

Abre sprint7_final_project_telecom_analysis.ipynb

Ejecuta las celdas en orden

Nota: Para la Opción 2, necesitarás clonar el repositorio y los archivos CSV deben estar en la carpeta data/ dentro del proyecto clonado. El repositorio incluye los archivos CSV necesarios para el análisis.

📦 Dependencias necesarias
¿Qué es esto y para qué sirve?

Las dependencias son las librerías de Python que el notebook necesita para funcionar correctamente. Instala estas librerías en tu entorno local (Jupyter Notebook) para que puedas ejecutar el análisis sin errores.

bash
pip install pandas numpy matplotlib seaborn
Nota: En Google Colab, estas librerías ya vienen preinstaladas, por lo que no es necesario ejecutar este comando en ese entorno.

📝 Licencia
Este proyecto fue desarrollado como parte de un ejercicio académico. Los datos son simulados y no representan información real de clientes.

🙋 Contacto
Para preguntas o comentarios sobre este análisis:

Estudiante: Sergio Pérez

Correo electrónico: spabiantun@gmail.com

Curso: TripleTen Bootcamp - Data Analyst

Instructor: Equipo de instrucción de TripleTen
