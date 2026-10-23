# Proyecto RetailPro — Análisis Comercial y Modelo de Datos

## Descripción del Proyecto

RetailPro es una solución de analítica de datos orientada al análisis de la información comercial de la empresa. El proyecto abarca desde el diseño y modelado de la base de datos relacional hasta la transformación de datos y creación de un modelo analítico que permite supervisar el rendimiento de ventas, el comportamiento de clientes y el rendimiento de productos.

## Objetivo General

El objetivo del proyecto es analizar la información comercial de RetailPro, con foco en el comportamiento de las ventas y los productos, para construir indicadores y visualizaciones que permitan comparar resultados entre períodos e identificar los principales factores que influyen en el desempeño comercial.

## Herramientas Utilizadas

* **SQL Server**: Sistema de gestión de bases de datos relacionales para el almacenamiento y modelado de datos.
* **SQL Server Management Studio (SSMS)**: Entorno de administración para la ejecución de scripts SQL, creación de tablas y consultas.
* **Power BI**: Herramienta utilizada para integrar los datos preparados en Power Query, establecer las relaciones entre las tablas, crear medidas DAX y desarrollar visualizaciones para analizar los resultados del proyecto.
* **Power Query**: Motor de transformación y limpieza de datos dentro de Power BI.
* **DAX (Data Analysis Expressions)**: Lenguaje de fórmulas utilizado para la creación de medidas e indicadores clave en el modelo analítico.

## Estructura de la Base de Datos

La base de datos contiene información integrada sobre las operaciones comerciales a través de las siguientes entidades principales:

* **clientes**: Almacena los datos demográficos y de registro de los clientes (`id\\\\\\\_cliente`, `nombre`, `email`, `ciudad`, `fecha\\\\\\\_registro`).
* **categorias**: Agrupa los productos según su clasificación comercial (`id\\\\\\\_categoria`, `nombre\\\\\\\_categoria`, `descripcion`).
* **productos**: Mantiene el catálogo de productos, su categoría asociada, precio, inventario y estado (`id\\\\\\\_producto`, `nombre\\\\\\\_producto`, `id\\\\\\\_categoria`, `precio`, `stock`, `activo`).
* **ventas**: Registra las transacciones comerciales realizadas, vinculando a los clientes y productos con el detalle de fecha, cantidades y precios (`id\\\\\\\_venta`, `id\\\\\\\_cliente`, `id\\\\\\\_producto`, `cantidad`, `precio\\\\\\\_unitario`, `fecha\\\\\\\_venta`).

\---

## Cómo Ejecutar los Scripts SQL

### Requisitos Previos

1. Tener instalado **SQL Server** y **SQL Server Management Studio (SSMS)**.
2. Contar con permisos para crear y modificar bases de datos.

### Pasos de Ejecución

1. **Clonar o descargar el repositorio:**

```bash
   git clone https://github.com/alddycanttos15-cyber/coder.git
   ```

2. **Abrir SSMS y conectarse al servidor SQL Server.**
3. **Abrir el script SQL del proyecto** desde el menú `File > Open > File...` en SSMS.
4. **Ejecutar el script:**

   * Hacer clic en el botón **Execute** (o presionar `F5`).
   * El script ventas\_tech\_db.sql crea la base de datos ventas\_tech\_DB, define las tablas categorias, clientes, productos y ventas, e inserta los datos iniciales. Luego, los scripts de consultas permiten analizar y relacionar la información cargada mediante consultas SQL.
5. **Verificar la creación:**

   * Ejecutar la siguiente consulta para validar la vista consolidada:

```sql
     USE ventas\\\\\\\_tech\\\\\\\_DB;
     SELECT \\\\\\\* FROM vw\\\\\\\_ventas\\\\\\\_consolidadas;
     ```



