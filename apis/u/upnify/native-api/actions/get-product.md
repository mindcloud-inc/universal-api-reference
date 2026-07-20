# Get Product with Upnify

Retrieves a product from Upnify.

## Endpoint

- **Method:** `GET`
- **Path:** `v4/catalogos/productos/:tkProducto`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [Get Product](https://desarrollo.upnify.com/api-rest/catalogos/#api-Productos-GetCatalogosProductosTkproducto)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tkProducto` | path | `string` | yes | El token que identifica a un producto en el sistema, del cual se requiere obtener los detalles.  ¿Dónde obtengo el token? |
