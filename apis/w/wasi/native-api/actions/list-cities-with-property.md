# List Cities With Property with Wasi

Retrieves cities with assigned properties from Wasi.

## Endpoint

- **Method:** `GET`
- **Path:** `/location/cities-with-property`
- **Base URL:** `https://api.wasi.co/v1`
- **Official documentation:** [List Cities With Property](https://api.wasi.co/docs/en/guide/cities.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `for_rent` | query | `boolean` | no | Only include rental inventory. |
| `for_sale` | query | `boolean` | no | Only include sale inventory. |
| `for_transfer` | query | `boolean` | no | Only include transfer inventory. |
| `id_property_type` | query | `number` | no | Limit cities to one property type. |
| `scope` | query | `number` | no | Choose which Wasi inventory scope to inspect. |
| `with_country` | query | `boolean` | no | Include country information when available. |
| `with_region` | query | `boolean` | no | Include region information when available. |
