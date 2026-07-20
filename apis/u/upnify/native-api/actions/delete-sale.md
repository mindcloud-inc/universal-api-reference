# Delete Sale with Upnify

Deletes an existing sale from Upnify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `v4/ventas/:tkVenta`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [Delete Sale](https://desarrollo.upnify.com/api-rest/ventas/#api-Ventas-DeleteVentasTkventa)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tkVenta` | path | `string` | yes | Código token que identifica de forma única a una venta en el sistema, la cual se requiere descartar.  ¿Dónde obtengo el token? |
