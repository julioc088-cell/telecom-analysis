#Objetivo del Proyecto
El objetivo principal de este proyecto es realizar un Análisis de Datos para entender el comportamiento de consumo de los usuarios de ConnectaTel. 
Se busca identificar patrones de uso, detectar anomalías y segmentar a los clientes por edad y nivel de actividad para proponer mejoras en la estrategia de planes comerciales (Básico vs. Premium).

#Datasets Utilizados
El análisis integra tres fuentes de datos principales:
Users (users_latam.csv): Información demográfica y perfil del usuario.
Columnas: user_id, age, city, plan, churn_date, etc.
Usage (usage.csv): Detalle del consumo mensual por usuario.
Columnas: user_id, cant_mensajes, cant_llamadas, cant_minutos_llamada.
Plans (plans.csv): Especificaciones técnicas y comerciales de cada plan.
Columnas: plan_name, usd_monthly_pay, minutes_included, messages_included, etc.

#Etapas del Análisis
Limpieza de Datos:
Identificación y manejo de valores nulos (especialmente en `churn_date`, `city`, `duration` y `length`).
Corrección de valores atípicos imposibles (valores `-999` en la columna `age`).
Análisis Exploratorio (EDA):
Visualización de distribuciones mediante Histogramas.
Identificación visual de outliers mediante Boxplots.
Tratamiento de Outliers:
Cálculo de límites estadísticos utilizando el método del Rango Intercuartílico (IQR).
Toma de decisiones sobre la permanencia de consumidores intensivos.
Segmentación:
Creación de `grupo_edad`: Joven, Adulto y Adulto Mayor.
Creación de `grupo_uso`: Bajo uso, Uso medio y Alto uso.
Insights y Visualización:
Gráficos de barras (`countplot`) para comparar segmentos y validar la estrategia comercial.

#Cómo ejecutar el Notebook (GitHub)
Visualización: Haz clic directamente en el archivo .ipynb dentro de este repositorio.

#Guía de Reproducción
Coloca los archivos plans.csv, users_latam.csv y usage.csv en la ruta /datasets/ (o ajusta las rutas en el código).
Ejecuta el notebook de manera secuencial.
Las visualizaciones de Boxplots se generarán automáticamente para las 4 variables principales de consumo.
