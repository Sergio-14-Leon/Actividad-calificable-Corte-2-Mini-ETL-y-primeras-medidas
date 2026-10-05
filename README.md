# Actividad Calificable · Corte 2 — Mini-ETL y primeras medidas

**Estudiante:** Sergio Leon  
**Asignatura:** Inteligencia de Negocios  
**Semana:** 04  

---

## Evidencias de Trabajo

### 1. Transformaciones en Power Query

paso1_powerquery.png

### 2. Medidas DAX y Contexto de Filtro

paso2_medidas_dax.png

---

## ETL Steps & Measures

In this project, a retail sales dataset was imported from a CSV file and processed through Power Query to improve data quality and analytical usability.

First, data types were standardized by converting transaction dates to the Date format, quantities to Whole Number, and sales values to Decimal Number. Second, null values detected in the product category field were replaced with "Unassigned" to avoid reporting inconsistencies. Third, duplicate sales transactions were removed using the transaction identifier `ID_Venta` as the unique key.

Next, product names were cleaned by removing extra spaces and applying proper capitalization. An additional calculated column called `Segmento_Cliente` was created to classify customers as "Frecuente" or "Ocasional" based on the number of purchases recorded.

Finally, three DAX measures were developed to monitor commercial performance:

- `Ventas Totales` using `SUM` to calculate overall revenue.
- `Promedio Venta` using `AVERAGE` to determine the average transaction amount.
- `Ingreso por Unidad` using `DIVIDE` to safely calculate revenue per item sold while handling division-by-zero scenarios.

These transformations and measures provide a reliable foundation for analyzing customer behavior, sales trends, and product performance through interactive Power BI reports.
