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

| Columna | Non-Null Count | Dtype |
| :--- | :--- | :--- |
| `sku` | 80 non-null | object |
| `product_name` | 80 non-null | object |
| `price_group_id` | 80 non-null | object |
| `price_group_name` | 80 non-null | object |
| `group_type` | 80 non-null | object |

---

## `eci_product_master.csv`

Es el catálogo maestro de productos. Contiene la jerarquía (categoría, grupo, subgrupo), la marca y los precios de cada artículo.

### Columnas

| Columna | Non-Null Count | Dtype |
| :--- | :--- | :--- |
| `sku` | 861 non-null | object |
| `product_name` | 861 non-null | object |
| `category` | 861 non-null | object |
| `group` | 861 non-null | object |
| `subgroup` | 861 non-null | object |
| `brand` | 861 non-null | object |
| `base_price` | 861 non-null | float64 |
| `initial_ticket_price` | 861 non-null | float64 |
| `costos` | 861 non-null | float64 |

---

## `eci_stores_clusters.csv`

Asigna cada tienda a un "cluster" o agrupación geográfica/estratégica.

### Columnas

| Columna | Non-Null Count | Dtype |
| :--- | :--- | :--- |
| `STORE_ID` | 157 non-null | object |
| `BRAND` | 157 non-null | object |
| `STORE_NAME` | 157 non-null | object |
| `CLUSTER` | 140 non-null | object |

---

## `eci_stores.csv`

Contiene información detallada de cada tienda, como su dirección, tipo, región y fechas de operación.

### Columnas

| Columna | Non-Null Count | Dtype |
| :--- | :--- | :--- |
| `STORE_ID` | 157 non-null | object |
| `BRAND` | 157 non-null | object |
| `STORE_NAME` | 157 non-null | object |
| `ADDRESS1` | 157 non-null | object |
| `ADDRESS2` | 43 non-null | object |
| `CITY` | 157 non-null | object |
| `STATE` | 157 non-null | object |
| `ZIP` | 151 non-null | object |
| `OPENDATE` | 157 non-null | object |
| `CLOSEDATE` | 18 non-null | object |
| `STORE_TYPE` | 155 non-null | object |
| `REGION` | 157 non-null | object |

---

## `eci_transactions.csv`

Este es el dataset principal con el registro de todas las transacciones de venta. Es el más grande en volumen.

### Columnas

| Columna | Non-Null Count | Dtype |
| :--- | :--- | :--- |
| `TRANSACTION_ID` | 19004759 non-null | int64 |
| `DATE` | 19004759 non-null | object |
| `STORE_ID` | 19004759 non-null | object |
| `SKU` | 19004759 non-null | object |
| `QUANTITY` | 19004759 non-null | float64 |
| `PRICE` | 19004759 non-null | float64 |
| `TOTAL_SALES` | 19004759 non-null | float64 |
| `SUBGROUP` | 19004759 non-null | object |
| `STORE_SUBGROUP_DATE_ID` | 19004759 non-null | object |

---

## `ids_test.csv`

Contiene los identificadores únicos (`STORE_SUBGROUP_DATE_ID`) que se utilizarán para generar el conjunto de datos de prueba para la predicción del modelo.

### Columnas

| Columna | Non-Null Count | Dtype |
| :--- | :--- | :--- |
| `STORE_SUBGROUP_DATE_ID` | 77700 non-null | object |

