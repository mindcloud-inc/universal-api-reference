# List Countries with Wasi

Retrieves countries from Wasi.

## Endpoint

- **Method:** `GET`
- **Path:** `/location/all-countries`
- **Base URL:** `https://api.wasi.co/v1`
- **Official documentation:** [List Countries](https://api.wasi.co/docs/en/guide/countries.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `for_rent` | query | `boolean` | no | Only count properties available for rent. |
| `for_sale` | query | `boolean` | no | Only count properties available for sale. |
| `for_transfer` | query | `boolean` | no | Only count properties available for transfer. |
| `id_property_type` | query | `number` | no | Limit quantity counts to one property type. |
| `quantity` | query | `boolean` | no | Include the number of matching properties per country. |
| `scope` | query | `number` | no | Choose which property scope to count. |
