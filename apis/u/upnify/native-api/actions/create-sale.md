# Create Sale with Upnify

Creates a new sale in Upnify.

## Endpoint

- **Method:** `POST`
- **Path:** `v4/ventas`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [Create Sale](https://desarrollo.upnify.com/api-rest/ventas/#api-Ventas-PostVentas)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tkProspecto` | body | `string` | yes | Código token del prospecto al que se agregará la venta.  ¿Dónde obtengo el token? |
| `tkFase` | body | `string` | yes | Código token que identificade forma única a una fase en el sistema.  ¿Dónde obtengo el token? |
| `tkLineaProducto` | body | `string` | yes | Código token que identificade forma única a una línea de productos en el sistema.  ¿Dónde obtengo el token? |
| `tkMoneda` | body | `string` | yes | Código token que identificade forma única a un tipo de moneda en el sistema.  ¿Dónde obtengo el token? |
| `tkCerteza` | body | `string` | yes | Código token que identificade forma única a una certeza en el sistema.  ¿Dónde obtengo el token? |
| `concepto` | body | `string` | yes | Identifica el concepto de la oportunidad. |
| `cantidad` | body | `number` | yes | Identifica la cantidad de productos/servicios de la venta. |
| `referencia` | body | `string` | yes | Identifica el motivo de la venta. |
| `fechaCierreVenta` | body | `date` | yes | Contiene un formato compuesto por fecha y hora que indica cuando se realizó la venta. |
| `monto` | body | `number` | yes | Cantidad monetaria con la que se generará la venta. |
| `anticiposMonto` | body | `number` | yes | Cantidad monetaria que indica el monto que estan pagando de la venta. |
| `anticiposComision` | body | `number` | yes | Cantidad monetaria que indica el monto que estan pagando de la comision de la venta. |
| `comision` | body | `number` | yes | Indica una cantidad de comision con base 1, (donde 1 es el 100%)por el la venta. |
| `comisionMonto` | body | `number` | yes | Cantidad monetaria que indica el monto total de comisión por la venta. |
| `saldoMonto` | body | `number` | yes | Cantidad monetaría que identifica el saldo pendiente de la venta. |
| `saldoComision` | body | `number` | yes | Cantidad monetaría que identifica el saldo pendiente de la comisión por la venta. |
| `productos` | body | `object` | yes | Arreglo de datos en las que se agregan los productos relacionados a la venta. |
| `pagos` | body | `object` | yes | Arreglo de datos en las que se agregan los pagos relacionados a la venta. |
| `tipoDeCambio` | body | `number` | yes | Indica el tipo de cambio con el que se generará la venta. |
| `tipoComision` | body | `number` | yes | Indica la forma en la que se pagarán las comisiones.  - 0 Prorrateadas.  - 1 Primer pago.  - 2 Último pago.  - 3 Manual. |
| `parcialidades` | body | `number` | yes | Indica el numero de parcialidades en las que se liquidará la venta. |
| `periodicidad` | body | `number` | yes | Indica la forma en la que se realizaran los pagos de la venta  - 1 Mensual.  - 2 Bimestral.  - 3 Trimestral.  - 4 Semestral.  - 5 Anual.  - 6 Otro.  - 7 Semanal.  - 8 Quincenal. |
| `montoPagado` | body | `number` | yes | Indica el monto que se esta pagando de la venta. |
| `descuento` | body | `number` | yes | Indica la cantidad monetaria del descuento realizado a la venta. |
| `descuentoPct` | body | `number` | yes | Almacena un valor con base 1, donde 1 es el 100%. Este valor indica el porcentaje del descuento. |
| `subtotal` | body | `number` | yes | Almacena una cantidad monetaria que indica el subtotal de la venta. |
| `impuestos` | body | `number` | yes | Almacena una cantidad monetaria que indica el monto total de los impuestos trasladados de la venta. |
| `impuestosRetenidos` | body | `number` | yes | Almacena una cantidad monetaria que indica el monto total de los impuestos retenidos de la venta. |
