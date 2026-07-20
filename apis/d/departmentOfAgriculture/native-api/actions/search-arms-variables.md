# Search ARMS Variables with Department of Agriculture

Finds ARMS variables in Department of Agriculture by ID, name, report, or group.

## Endpoint

- **Method:** `GET`
- **Path:** `/arms/variable`
- **Base URL:** `https://api.ers.usda.gov/data`
- **Official documentation:** [Search ARMS Variables](https://www.ers.usda.gov/developer/data-apis/arms-data-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Filter variables by ARMS variable abbreviation or identifier. |
| `name` | query | `string` | no | Filter variables by display name. |
| `report` | query | `string` | no | Filter variables by ARMS report number or report name. |
| `group` | query | `number` | no | Filter variables by ARMS variable group. |
