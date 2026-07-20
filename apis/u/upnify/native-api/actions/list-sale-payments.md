# List Sale Payments with Upnify

Retrieves payments for a sale in Upnify.

## Endpoint

- **Method:** `GET`
- **Path:** `v4/ventas/:tkVenta/cobros`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [List Sale Payments](https://desarrollo.upnify.com/api-rest/ventas/#api-Ventas-GetVentasTkventaCobros)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tkVenta` | path | `string` | yes | El código token que identifica a una venta de manera única dentro del CRM, del cual se requiere obtener la lista de los cobros asociados.  ¿Dónde obtengo el token? |
