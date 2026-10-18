# Reto Big Data - Grupo 4: Análisis de Banderas Azules

Este repositorio contiene el trabajo desarrollado por el Grupo 4 para el reto de la Sesión 04 de Sistemas de Big Data. El objetivo consiste en extraer, transformar y analizar los datos correspondientes a las banderas azules en las playas y puertos de Andalucía.

## 👥 Equipo y Roles

El trabajo se ha distribuido en los siguientes roles:
* **Fuente:** José María López González
* **Carga:** Lucas Faura Martín
* **Transformación:** Sergii Butrii, Jose Maria
* **Cierre:** Samuel Márquez Ruiz

## 📊 Sobre el Dataset

* **Temática:** Medio ambiente.
* **Organismo:** Junta de Andalucía.
* **Licencia:** Reconocimiento 4.0 Internacional (CC BY 4.0).
* **Formato Original:** CSV.
* **Detalles Técnicos:** El archivo original contiene 633 registros de datos, utiliza el punto y coma (`;`) como separador y tiene codificación `cp1250`.

## 📁 Archivos del Repositorio

* **`medio_ambiente.ipynb`**: Cuaderno de Jupyter con el código en Python utilizado para hacer la petición web, explorar los datos (identificación de nulos, tipos y dimensiones) y aplicar las transformaciones necesarias usando la librería `pandas`.
* **`reto-BIG-DATA-Grupo4.pdf`**: Ficha original del reto con las instrucciones, la asignación de tareas del grupo y los metadatos requeridos.

## 🛠️ Fases del Procesamiento (ETL)

El script implementado en el cuaderno realiza las siguientes fases principales:

1. **Carga y Exploración:** Descarga del CSV en memoria, detección de codificación óptima, y análisis preliminar (filas, columnas, nulos y tipos de datos).
2. **Transformaciones Aplicadas:**
   * Limpieza de espacios innecesarios en los nombres de las columnas.
   * Eliminación de registros duplicados.
   * Descarte de columnas irrelevantes o con un alto índice de valores nulos (columna `Notas`).
   * Corrección de la tipografía de cabeceras (cambio de `Ańo` a `Año`).
   * Separación de la columna de años en dos variables independientes (`Año inicio` y `Año final`) transformadas a formato numérico (entero).
   * Ordenación final del *dataframe* estructurada por `Provincia` (ascendente) y `Año inicio` (descendente).
