# Create a single fact table filter with GrowthBook

Creates a fact table filter in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/fact-tables/:factTableId/filters`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create a single fact table filter](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `factTableId` | path | `string` | yes | Specify a specific fact table |
| `name` | body | `string` | yes | — |
| `description` | body | `string` | no | Description of the fact table filter |
| `value` | body | `string` | yes | The SQL expression for this filter. |
| `managedBy` | body | `string` | no | Set this to "api" to disable editing in the GrowthBook UI. Before you do this, the Fact Table itself must also be marked as "api" |
