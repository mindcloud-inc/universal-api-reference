# List Properties with Wasi

Finds properties in Wasi by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/property/search`
- **Base URL:** `https://api.wasi.co/v1`
- **Official documentation:** [List Properties](https://api.wasi.co/docs/en/guide/properties.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `match` | query | `string` | no | Keywords to search across properties. |
| `id_country` | query | `number` | no | Filter by Wasi country identifier. |
| `title` | query | `string` | no | Filter by a partial or full property title. |
| `id_property` | query | `number` | no | Return a specific property by its Wasi identifier. |
| `id_region` | query | `number` | no | Filter by Wasi region identifier. |
| `id_city` | query | `number` | no | Filter by Wasi city identifier. |
| `id_location` | query | `number` | no | Filter by Wasi location identifier. |
| `id_property_type` | query | `number` | no | Filter by Wasi property type identifier. |
| `for_sale` | query | `boolean` | no | Only return properties available for sale. |
| `for_rent` | query | `boolean` | no | Only return properties available for rent. |
| `for_transfer` | query | `boolean` | no | Only return properties available for transfer. |
| `scope` | query | `number` | no | Choose whether to include your own properties, allies, all, or group results. |
| `short` | query | `boolean` | no | Exclude galleries and features from the response when true. |
| `lax_business_type` | query | `boolean` | no | When true, return properties matching any selected business type instead of all selected business types. |
