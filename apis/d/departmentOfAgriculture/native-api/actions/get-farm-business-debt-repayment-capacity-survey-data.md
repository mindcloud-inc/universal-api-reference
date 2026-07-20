# Get Farm Business Debt Repayment Capacity Survey Data with Department of Agriculture

Retrieves Farm Business Debt Repayment Capacity survey data from Department of Agriculture.

## Endpoint

- **Method:** `GET`
- **Path:** `/arms/surveydata`
- **Base URL:** `https://api.ers.usda.gov/data`
- **Official documentation:** [Get Farm Business Debt Repayment Capacity Survey Data](https://www.ers.usda.gov/developer/data-apis/arms-data-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | yes | ARMS survey year. |
| `variable` | query | `string` | no | Optional ARMS variable abbreviation. |
| `state` | query | `string` | no | Optional state filter. |
| `farmType` | query | `string` | no | Optional farm type filter. |
