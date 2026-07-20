# Get a single fact filter with GrowthBook

Retrieves a fact table filter from GrowthBook.

## Endpoint

- **Method:** `GET`
- **Path:** `/fact-tables/:factTableId/filters/:id`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Get a single fact filter](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `factTableId` | path | `string` | yes | Specify a specific fact table |
| `id` | path | `string` | yes | The id of the requested resource |
