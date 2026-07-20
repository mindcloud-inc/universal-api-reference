# List Sale Products with Upnify

Retrieves products for a sale in Upnify.

## Endpoint

- **Method:** `GET`
- **Path:** `v4/ventas/:tkVenta/productos`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [List Sale Products](https://desarrollo.upnify.com/api-rest/ventas/#api-Ventas-GetVentasTkventaProductos)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tkVenta` | path | `string` | yes | Identificador unico de una venta en el sistema, del cual se requiere obtener los productos asociados.  ¿Dónde obtengo el token? |
