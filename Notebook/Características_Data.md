# Características de cada DataSet

## eci_customer_data

Contiene información de los clientes de la empresa. Puede ser importante para sugerencias o recomendaciones para usuarios de manera particular


### Columnas

| Columna       | Descripción                                | Tipo de Dato | Notas                |
|---------------|--------------------------------------------|--------------|----------------------|
| `customer_id` | Identificador único para cada cliente.     | `string`     | Clave primaria       |
| `name`        | Nombre del cliente.                        | `string`     |                      |
| `email`       | Correo electrónico del cliente.            | `string`     | Puede contener nulos |
| `city`        | Ciudad de residencia del cliente.          | `string`     |                      |
| `signup_date` | Fecha en la que el cliente se registró.    | `date`       | Formato YYYY-MM-DD   |

