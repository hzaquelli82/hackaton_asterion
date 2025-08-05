# Características de cada DataSet

## `eci_customer_data.csv`

Contiene información demográfica y de lealtad de los clientes. Es fundamental para entender el perfil de los compradores y para segmentaciones.

### Columnas

| Columna | Non-Null Count | Dtype | Descripcion |
| :--- | :--- | :--- | :--- |
| `client_id` | 801923 non-null | int64 | Identificador único del cliente |
| `phone_number` | 705749 non-null | object | Nñumero de teléfono del cliente |
| `email_address` | 657079 non-null | object | Dirección de correo electrónico del cliente |
| `city` | 801923 non-null | object | Ciudad del cliente |
| `state` | 801923 non-null | object | Estado del cliente |
| `zip_code` | 734663 non-null | object | Código postal del cliente |
| `education_level` | 682042 non-null | object | Nivel educativo del cliente |
| `occupation` | 657407 non-null | object | Ocupación del cliente |
| `loyalty_member` | 762074 non-null | object | Si el cliente es miembro de la lealtad |
| `loyalty_number` | 440681 non-null | object | Número de lealtad del cliente |
| `loyalty_points` | 392749 non-null | object | Puntos de lealtad del cliente |


---

## `eci_product_groups.csv`

Define agrupaciones de productos, probablemente para estrategias de marketing como bundles, promociones o productos sustitutos.

### Columnas

| Columna | Non-Null Count | Dtype | Descripción |
| :--- | :--- | :--- | :--- |
| `sku` | 80 non-null | object | Código de producto |
| `product_name` | 80 non-null | object | Nombre del Producto |
| `price_group_id` | 80 non-null | object | ID del grupo de producto |
| `price_group_name` | 80 non-null | object | Nombre del grupo de producto |
| `group_type` | 80 non-null | object | Tipo de grupo de producto |


---

## `eci_product_master.csv`

Es el catálogo maestro de productos. Contiene la jerarquía (categoría, grupo, subgrupo), la marca y los precios de cada artículo.

### Columnas

| Columna | Non-Null Count | Dtype | Descripción |
| :--- | :--- | :--- | :--- |
| `sku` | 861 non-null | object | Código de producto |
| `product_name` | 861 non-null | object | Nombre del producto |
| `category` | 861 non-null | object | Categoría del producto |
| `group` | 861 non-null | object | Grupo del producto |
| `subgroup` | 861 non-null | object | Subgrupo del producto |
| `brand` | 861 non-null | object | Marca del producto |
| `base_price` | 861 non-null | float64 | Precio base del producto |
| `initial_ticket_price` | 861 non-null | float64 | Precio inicial de venta del producto |
| `costos` | 861 non-null | float64 | Costos del producto |


---

## `eci_stores_clusters.csv`

Asigna cada tienda a un "cluster" o agrupación geográfica/estratégica.

### Columnas

| Columna | Non-Null Count | Dtype | Descripción |
| :--- | :--- | :--- | :--- |
| `STORE_ID` | 157 non-null | object | Identificador único de la tienda |
| `BRAND` | 157 non-null | object | Marca de la tienda |
| `STORE_NAME` | 157 non-null | object | Nombre de la tienda |
| `CLUSTER` | 140 non-null | object | Cluster geográfico al que pertenece la tienda |


---

## `eci_stores.csv`

Contiene información detallada de cada tienda, como su dirección, tipo, región y fechas de operación.

### Columnas

| Columna | Non-Null Count | Dtype | Descripción |
| :--- | :--- | :--- | :--- |
| `STORE_ID` | 157 non-null | object | Identificador único de la tienda |
| `BRAND` | 157 non-null | object | Marca de la tienda |
| `STORE_NAME` | 157 non-null | object | Nombre de la tienda |
| `ADDRESS1` | 157 non-null | object | Dirección de la tienda |
| `ADDRESS2` | 43 non-null | object | Dirección adicional de la tienda |
| `CITY` | 157 non-null | object | Ciudad de la tienda |
| `STATE` | 157 non-null | object | Estado de la tienda |
| `ZIP` | 151 non-null | object | Código postal de la tienda |
| `OPENDATE` | 157 non-null | object | Fecha de apertura de la tienda |
| `CLOSEDATE` | 18 non-null | object | Fecha de cierre de la tienda |
| `STORE_TYPE` | 155 non-null | object | Tipo de tienda |
| `REGION` | 157 non-null | object | Región de la tienda |


---

## `eci_transactions.csv`

Este es el dataset principal con el registro de todas las transacciones de venta. Es el más grande en volumen.

### Columnas

| Columna | Non-Null Count | Dtype | Descripción |
| :--- | :--- | :--- | :--- |
| `TRANSACTION_ID` | 19004759 non-null | int64 | Identificador único de la transacción |
| `DATE` | 19004759 non-null | object | Fecha de la transacción |
| `STORE_ID` | 19004759 non-null | object | Identificador de la tienda |
| `SKU` | 19004759 non-null | object | Código de producto |
| `QUANTITY` | 19004759 non-null | float64 | Cantidad vendida |
| `PRICE` | 19004759 non-null | float64 | Precio unitario del producto |
| `TOTAL_SALES` | 19004759 non-null | float64 | Total de ventas |
| `SUBGROUP` | 19004759 non-null | object | Subgrupo del producto |
| `STORE_SUBGROUP_DATE_ID` | 19004759 non-null | object | Identificador generado con tienda, subgrupo y fecha |


---

## `ids_test.csv`

Contiene los identificadores únicos (`STORE_SUBGROUP_DATE_ID`) que se utilizarán para generar el conjunto de datos de prueba para la predicción del modelo.

### Columnas

| Columna | Non-Null Count | Dtype |
| :--- | :--- | :--- |
| `STORE_SUBGROUP_DATE_ID` | 77700 non-null | object |

