# Search ARMS Reports with Department of Agriculture

Finds ARMS reports in Department of Agriculture by ID or name.

## Endpoint

- **Method:** `GET`
- **Path:** `/arms/report`
- **Base URL:** `https://api.ers.usda.gov/data`
- **Official documentation:** [Search ARMS Reports](https://www.ers.usda.gov/developer/data-apis/arms-data-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | no | Filter reports by numeric report ID from the ARMS report list. |
| `name` | query | `string` | no | Filter reports by report name. |
