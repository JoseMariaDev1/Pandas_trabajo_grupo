# Reto Big Data - Grupo 4: Análisis de Banderas Azules

Este repositorio contiene el trabajo desarrollado por el Grupo 4 para el reto de la Sesión 04 de Sistemas de Big Data[cite: 2]. El objetivo consiste en extraer, transformar y analizar los datos correspondientes a las banderas azules en las playas y puertos de Andalucía[cite: 2].

## 👥 Equipo y Roles

El trabajo se ha distribuido en los siguientes roles[cite: 3]:
* **Fuente:** José María López González[cite: 3]
* **Carga:** Lucas Faura Martín[cite: 3]
* **Transformación:** Sergii Butrii, Jose Maria[cite: 3]
* **Cierre:** Samuel Márquez Ruiz [cite: 3]

## 📊 Sobre el Dataset

* **Temática:** Medio ambiente[cite: 2].
* **Organismo:** Junta de Andalucía[cite: 3].
* **Licencia:** Reconocimiento 4.0 Internacional (CC BY 4.0)[cite: 3].
* **Formato Original:** CSV[cite: 3].
* **Detalles Técnicos:** El archivo original contiene 633 registros de datos[cite: 1], utiliza el punto y coma (`;`) como separador y tiene codificación `cp1250`[cite: 1, 3].

## 📁 Archivos del Repositorio

* **`medio_ambiente.ipynb`**: Cuaderno de Jupyter con el código en Python utilizado para hacer la petición web, explorar los datos (identificación de nulos, tipos y dimensiones) y aplicar las transformaciones necesarias usando la librería `pandas`[cite: 1].
* **`reto-BIG-DATA-Grupo4.pdf`**: Ficha original del reto con las instrucciones, la asignación de tareas del grupo y los metadatos requeridos[cite: 2, 3].

## 🛠️ Fases del Procesamiento (ETL)

El script implementado en el cuaderno realiza las siguientes fases principales[cite: 1]:

1. **Carga y Exploración:** Descarga del CSV en memoria, detección de codificación óptima, y análisis preliminar (filas, columnas, nulos y tipos de datos)[cite: 1].
2. **Transformaciones Aplicadas:**
   * Limpieza de espacios innecesarios en los nombres de las columnas[cite: 1].
   * Eliminación de registros duplicados[cite: 1].
   * Descarte de columnas irrelevantes o con un alto índice de valores nulos (columna `Notas`)[cite: 1].
   * Corrección de la tipografía de cabeceras (cambio de `Ańo` a `Año`)[cite: 1].
   * Separación de la columna de años en dos variables independientes (`Año inicio` y `Año final`) transformadas a formato numérico (entero)[cite: 1].
   * Ordenación final del *dataframe* estructurada por `Provincia` (ascendente) y `Año inicio` (descendente)[cite: 1].
