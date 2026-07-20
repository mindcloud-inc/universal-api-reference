# Search ARMS Categories with Department of Agriculture

Finds ARMS categories in Department of Agriculture by ID or name.

## Endpoint

- **Method:** `GET`
- **Path:** `/arms/category`
- **Base URL:** `https://api.ers.usda.gov/data`
- **Official documentation:** [Search ARMS Categories](https://www.ers.usda.gov/developer/data-apis/arms-data-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Filter categories by ARMS category abbreviation. |
| `name` | query | `string` | no | Filter categories by category display name. |
