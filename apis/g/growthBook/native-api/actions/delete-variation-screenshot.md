# Delete a variation screenshot with GrowthBook

Deletes a variation screenshot from GrowthBook.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/experiments/:id/variation/:variationId/screenshot`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Delete a variation screenshot](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `variationId` | path | `string` | yes | — |
| `path` | body | `string` | yes | The screenshot path/URL to delete (from upload response) |
