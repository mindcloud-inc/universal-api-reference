# List Property Types with Wasi

Retrieves property types from Wasi.

## Endpoint

- **Method:** `GET`
- **Path:** `/property-type/all`
- **Base URL:** `https://api.wasi.co/v1`
- **Official documentation:** [List Property Types](https://api.wasi.co/docs/en/guide/properties.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `for_rent` | query | `boolean` | no | Only count rental inventory. |
| `for_sale` | query | `boolean` | no | Only count sale inventory. |
| `for_transfer` | query | `boolean` | no | Only count transfer inventory. |
| `quantity` | query | `boolean` | no | Include the number of matching properties per property type. |
