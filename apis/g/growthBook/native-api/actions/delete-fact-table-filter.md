# Deletes a single fact table filter with GrowthBook

Deletes a fact table filter from GrowthBook.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/fact-tables/:factTableId/filters/:id`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Deletes a single fact table filter](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `factTableId` | path | `string` | yes | Specify a specific fact table |
| `id` | path | `string` | yes | The id of the requested resource |
