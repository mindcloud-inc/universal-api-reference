# Get ARMS Survey Data by Report with Department of Agriculture

Retrieves ARMS survey data by report from Department of Agriculture.

## Endpoint

- **Method:** `GET`
- **Path:** `/arms/surveydata`
- **Base URL:** `https://api.ers.usda.gov/data`
- **Official documentation:** [Get ARMS Survey Data by Report](https://www.ers.usda.gov/developer/data-apis/arms-data-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | yes | ARMS survey year. |
| `report` | query | `string` | yes | ARMS report number or report name. |
| `variable` | query | `string` | no | Optional ARMS variable abbreviation such as `kount`. |
| `state` | query | `string` | no | Optional state code/name; provider defaults to all survey states. |
| `farmType` | query | `string` | no | Optional farm type filter. |
| `category` | query | `string` | no | Optional primary category. |
| `categoryValue` | query | `string` | no | Optional primary category value. |
| `category2` | query | `string` | no | Optional secondary category. |
| `category2Value` | query | `string` | no | Optional secondary category value. |
| `subReport` | query | `number` | no | Optional ARMS sub-report ID. |
