# Search ARMS Farm Types with Department of Agriculture

Finds ARMS farm types in Department of Agriculture by ID or name.

## Endpoint

- **Method:** `GET`
- **Path:** `/arms/farmtype`
- **Base URL:** `https://api.ers.usda.gov/data`
- **Official documentation:** [Search ARMS Farm Types](https://www.ers.usda.gov/developer/data-apis/arms-data-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | no | Filter farm types by numeric ID. |
| `name` | query | `string` | no | Filter farm types by display name. |
