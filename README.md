# GRUPOBD_CIIN1021P_EF_REPO

# Proyecto Integrador: DataSalud Perú - DIRESA La Libertad

## Descripción del Proyecto

Este repositorio contiene los artefactos técnicos desarrollados para el sistema integrado de base de datos segura, automatizada e inteligente para la Dirección Regional de Salud La Libertad, utilizando los datos abiertos del MINSA.

## Estructura del Repositorio

El código y los entregables están organizados estrictamente por bloques temáticos:
- /automatizacion: Contiene los scripts SQL de procedimientos almacenados (con TRY/CATCH y transacciones), triggers de auditoría y funciones.
- /seguridad: Incluye los scripts SQL para la creación de roles (administrador, analista, auditor), políticas de respaldo (script de restore) y verificación de normativas.
- /BI: Almacena los scripts ETL, el diagrama/DDL del modelo dimensional (Data Warehouse bajo metodología Kimball) y el archivo del dashboard.
- /BigData: Contiene el notebook de PySpark (.ipynb) utilizado para el análisis de eficiencia y escalabilidad.

## Herramientas Requeridas

Todas las herramientas utilizadas en este proyecto son de uso gratuito, de código abierto o se ejecutaron en su capa gratuita:
- Gestor Relacional: SQL Server
- Gestor NoSQL: MongoDB
- Entorno Big Data: PySpark ejecutado en (indicar si usaron Google Colab, local o Databricks)
- Inteligencia de Negocios: Power BI Desktop 

## Instrucciones de Ejecución

Sigue estos pasos para desplegar el proyecto en un entorno local:
- Bloque de Automatización: Ejecutar primero los scripts de la carpeta /automatizacion para crear las tablas principales, los procedimientos almacenados y los triggers.
- Bloque de Seguridad: Ejecutar los scripts de la carpeta /seguridad para establecer los roles, asignar permisos y simular la política de backups.
- Bloque de BI: Correr el script ETL de la carpeta /BI para poblar el Data Warehouse. Luego, abrir el archivo del dashboard para visualizar los KPIs.
- Bloque de Big Data: Subir el notebook de la carpeta /BigData a tu entorno (por ejemplo, Google Colab), cargar el dataset del MINSA y ejecutar las celdas secuencialmente.
