# Update Opportunity with Upnify

Updates an existing opportunity in Upnify.

## Endpoint

- **Method:** `PUT`
- **Path:** `v4/oportunidades/:tkOportunidad`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [Update Opportunity](https://desarrollo.upnify.com/api-rest/oportunidades/#api-Oportunidades-PutOportunidadesTkoportunidad)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tkOportunidad` | path | `string` | yes | El código token que identifica a una oportunidad de manera única dentro del CRM, la cual se requiere modificar.  ¿Dónde obtengo el token? |
| `tkFase` | body | `string` | yes | Código token que identificade forma única a una fase en el sistema.  ¿Dónde obtengo el token? |
| `tkLineaProducto` | body | `string` | yes | Código token que identificade forma única a una línea de productos en el sistema.  ¿Dónde obtengo el token? |
| `tkMoneda` | body | `string` | yes | Código token que identificade forma única a un tipo de moneda en el sistema.  ¿Dónde obtengo el token? |
| `tkCerteza` | body | `string` | yes | Código token que identificade forma única a una certeza en el sistema.  ¿Dónde obtengo el token? |
| `concepto` | body | `string` | yes | Contiene el título o nombre de la nueva oportunidad. |
| `cierreEstimado` | body | `date` | yes | Contiene un formato compuesto de fecha y hora que indica la fecha estimada en la que se concretará la oportunidad. |
| `monto` | body | `number` | yes | Almacena una cantidad monetaria que indica el monto de la oportunidad. |
| `cantidad` | body | `number` | yes | Almacena la cantidad total de productos vendidos. |
| `subtotal` | body | `number` | yes | Almacena una cantidad monetaria que indica el subtotal de la oportunidad. |
| `comision` | body | `number` | yes | Almacena un valor con base 1, donde 1 es el 100%. Este valor indica el porcentaje de una comisión. |
| `comisionMonto` | body | `number` | yes | Indica la cantidad monetaria de la comisión. |
| `descuento` | body | `number` | yes | Indica la cantidad monetaria del descuento realizado a la oportunidad. |
| `descuentoPct` | body | `number` | yes | Almacena un valor con base 1, donde 1 es el 100%. Este valor indica el porcentaje del descuento. |
| `impuestos` | body | `number` | yes | Almacena una cantidad monetaria que indica el monto total de los impuestos trasladados de la oportunidad. |
| `impuestosRetenidos` | body | `number` | yes | Almacena una cantidad monetaria que indica el monto total de los impuestos retenidos de la oportunidad. |
| `productos` | body | `object` | yes | Arreglo de datos en las que se agregan los productos relacionados a la oportunidad. |
