# List Opportunity Products with Upnify

Retrieves products for an opportunity in Upnify.

## Endpoint

- **Method:** `GET`
- **Path:** `v4/oportunidades/:tkOportunidad/productos`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [List Opportunity Products](https://desarrollo.upnify.com/api-rest/oportunidades/#api-Oportunidades-GetOportunidadesTkoportunidadProductos)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tkOportunidad` | path | `string` | yes | El Identificador unico de una oportunidad dentro del CRM, de la cual se requiere conocer la lista de productos asociados.  ¿Dónde obtengo el token? |
