# Get ARMS Survey Data with Department of Agriculture

Retrieves ARMS survey data from Department of Agriculture.

## Endpoint

- **Method:** `GET`
- **Path:** `/arms/surveydata`
- **Base URL:** `https://api.ers.usda.gov/data`
- **Official documentation:** [Get ARMS Survey Data](https://www.ers.usda.gov/developer/data-apis/arms-data-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | yes | ARMS survey year. |
| `report` | query | `string` | yes | ARMS report number or report name. |
| `variable` | query | `string` | no | ARMS variable abbreviation such as `kount`. |
| `state` | query | `string` | no | State code/name; provider defaults to all survey states. |
| `farmType` | query | `string` | no | Farm type filter; provider defaults to All Farms. |
| `category` | query | `string` | no | Primary ARMS category abbreviation or name. |
| `categoryValue` | query | `string` | no | Primary category value; provider defaults to Total when category is used. |
| `category2` | query | `string` | no | Secondary ARMS category abbreviation or name. |
| `category2Value` | query | `string` | no | Secondary category value; provider defaults to Total when category2 is used. |
| `subReport` | query | `number` | no | Optional ARMS sub-report ID. |
