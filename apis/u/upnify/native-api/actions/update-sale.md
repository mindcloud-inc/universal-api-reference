# Update Sale with Upnify

Updates an existing sale in Upnify.

## Endpoint

- **Method:** `PUT`
- **Path:** `v4/ventas/:tkVenta`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [Update Sale](https://desarrollo.upnify.com/api-rest/ventas/#api-Ventas-PutVentasTkventa)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tkVenta` | path | `string` | yes | El código token que identifica a una venta de manera única dentro del CRM, y a la cual se requiere modificar..  ¿Dónde obtengo el token? |
| `comision` | body | `number` | yes | Indica el monto de la comisión ganada. |
| `referencia` | body | `string` | yes | Indica la referencia establecida para la venta. |
| `anticiposMonto` | body | `number` | yes | Indica un monto de un anticipo. |
| `anticiposComision` | body | `number` | yes | Indica el monto de un anticipo. |
| `saldoMonto` | body | `number` | yes | Contiene el monto del saldo de la venta en caso de existir anticipos o parcialidades. |
| `parcialidades` | body | `number` | yes | Indica el número de parcialidades de una venta. |
| `cantidad` | body | `number` | yes | Indica la cantidad de productos de la venta. |
| `tkmoneda` | body | `string` | yes | Código token que pertenece a una moneda registrada en el sistema. |
| `tipoDeCambio` | body | `number` | yes | Indica el valor de cambio de la moneda utilizada. |
