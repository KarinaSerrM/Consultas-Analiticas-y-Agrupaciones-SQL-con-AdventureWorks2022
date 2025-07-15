# Consultas Analíticas y Agrupaciones SQL con AdventureWorks2022

Este repositorio documenta una serie de ejercicios avanzados en SQL utilizando la base de datos AdventureWorks2022. Se desarrollan consultas que emplean funciones analíticas, cláusulas de agrupamiento, filtros condicionales y numeración de registros para mejorar la interpretación de los datos comerciales.

## Objetivo

Practicar operaciones SQL para obtener métricas agregadas, clasificaciones y rankings sobre las tablas de ventas de AdventureWorks2022, usando funciones de ventana y comandos especializados.

## Consultas implementadas

### 1. Agrupación y sumas
- `GROUP BY ProductID` con `SUM(OrderQty)` y `SUM(LineTotal)`
- Filtro con `HAVING SUM(LineTotal) > 5000`

### 2. Funciones analíticas
- `OVER (PARTITION BY SalesOrderID)` para total por pedido
- `ROW_NUMBER()` para numerar líneas por detalle de pedido
- `RANK()` para asignar jerarquía por valor de venta descendente
- `DENSE_RANK()` aplicado por producto con valores repetidos

### 3. Presentación de resultados
- Ordenamiento por `ORDER BY` para facilitar jerarquías
- Uso de expresiones como `CASE`, `COALESCE`, `ISNULL` para tratar valores nulos

## Herramientas utilizadas

- SQL Server (AdventureWorks2022)  
- SQL Management Studio  
- Scripts `.sql` ordenados por tipo de operación

## Estructura del repositorio

- `/consultas`: archivos SQL categorizados  
- `/visualizaciones`: capturas de resultados o tablas finales  
- `/README.md`: guía del proyecto con explicación técnica

## Conclusiones

- Las funciones de ventana permiten enriquecer la lógica de análisis por partición.
- Las cláusulas `GROUP BY` y `HAVING` son esenciales para sumarizaciones comerciales.
- Las jerarquías mediante `RANK`, `DENSE_RANK` y `ROW_NUMBER` aportan contexto estructurado.
- El tratamiento de nulos mejora la calidad semántica de los resultados.
