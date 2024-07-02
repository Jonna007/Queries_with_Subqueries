# PROYECTO Queries with Subqueries

## INVOICE Database

### 1. Número total de facturas realizadas por cada cliente

#### SQL:
```sql
SELECT 
    c.fullname AS nombre_cliente,
    c.address AS direccion,
    COUNT(i.id) AS nro_facturas
FROM 
    client c
JOIN 
    invoice i ON c.id = i.client_id
GROUP BY 
    c.fullname, c.address;
