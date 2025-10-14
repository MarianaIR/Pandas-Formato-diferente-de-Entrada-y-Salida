
# 🐼 PANDAS: MANEJO DE FORMATOS DE ENTRADA Y SALIDA (JSON/CSV)

[![Python](https://img.shields.io/badge/Python-3670A0?style=flat&logo=python&logoColor=ffdd54)](https://www.python.org/)  
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)](https://pandas.pydata.org/)  
[![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)](https://numpy.org/)  
[![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-333333?style=flat&logo=sqlalchemy&logoColor=white)](https://www.sqlalchemy.org/)

Este proyecto se centra en las **capacidades de la librería Pandas** para manejar y transformar datos provenientes de **diferentes formatos de entrada y salida**, demostrando su flexibilidad en la ingestión de datos web (JSON) y la interacción con bases de datos (SQL).

---

## 🧠 Contenido del Proyecto

### 1️⃣ Entrada de Datos desde la Web (JSON)
- **Carga de Datos Externos:** Se simula la extracción de información (como archivos de alumnos para una escuela) desde la web, destacando que los datos pueden venir en diversos formatos como **TXT, Excel, o a través de APIs (JSON)**.
- **Uso de JSON:** El ejercicio muestra cómo **Pandas** puede leer directamente archivos **JSON** desde una URL utilizando `pd.read_json()`.
- **Estructura del DataFrame:** El resultado es un **DataFrame de Pandas** que contiene datos como `Address`, `City`, `Country`, `Employees`, `ID`, `Name`, y `State`.

### 2️⃣ Preparación y Transformación de Datos
- **Creación de Columnas:** Se añaden nuevas columnas al DataFrame, como `Employees_Names` (con nombres de ejemplo).
- **Manejo de Cadenas (Strings):** Se demuestra cómo **manipular y combinar columnas** para crear datos derivados, como la generación de una columna de `Email` concatenando los nombres de los empleados con un dominio (ej. `@dominiodeemail.com`).
- **Lectura de Otros Formatos:** Se lee una segunda base de datos, `cursos.csv`, demostrando la capacidad de Pandas para manejar múltiples fuentes de datos.
- **Limpieza de Datos:** Se borran columnas que no se utilizarán del DataFrame de cursos (ej. `Sep 2023`, `Sep 2022`, `Change`).

### 3️⃣ Salida de Datos y Relación con SQL
- **Conexión a Base de Datos:** Se utiliza la librería **SQLAlchemy** para crear un **motor de base de datos** en memoria (`sqlite:///:memory:`).
- **Exportación a SQL:** Se demuestra cómo la función `to_sql()` de Pandas puede exportar directamente un DataFrame (`matriculas_por_curso`) a una tabla dentro del motor SQL creado.
- **Consultas (Querying) con Pandas:** Se realiza una consulta avanzada utilizando `.query()` y operaciones de `join` (`.set_index().join()`) para relacionar las tablas de empleados y cursos, identificando los nombres de los empleados matriculados en un curso específico (ej. ID de curso = 6, que es JavaScript).

---

## 🛠️ Librerías Utilizadas

| Librería       | Uso principal                               |
|----------------|---------------------------------------------|
| **Pandas**     | Carga, manipulación (lectura de JSON/CSV, `to_sql`) y análisis de datos|
| **NumPy**      | Utilizado para generar números aleatorios en la creación de datos de ejemplo|
| **SQLAlchemy** | Creación del motor SQL (`create_engine`) para demostrar la exportación de DataFrames a bases de datos|

---

## 🎯 Objetivo del Proyecto
Demostrar la **capacidad de Pandas para integrar datos** de múltiples fuentes y formatos (especialmente web/JSON), manipularlos eficientemente mediante operaciones de *Data Wrangling* (creación de emails, limpieza) y, finalmente, mostrar su **interoperabilidad con sistemas de bases de datos (SQL)** para el almacenamiento y la consulta de la información.

---

## 📈 Resultados Clave
- Se cargó con éxito una fuente de datos **JSON externa** a un DataFrame de Pandas.
- Se demostró la capacidad de generar *features* (como emails) y **limpiar DataFrames** (eliminación de columnas).
- Se logró **exportar datos de Pandas a un motor SQL** en memoria.
- Se pudo **relacionar información de diferentes DataFrames** usando técnicas de unión (`join`) para responder a preguntas específicas de negocio (ej. ¿Quién está en la clase de JavaScript?).

---
