# Insert to Series with Recombee

Adds items to a series in Recombee.

## Endpoint

- **Method:** `POST`
- **Path:** `/series/:seriesId/items/`
- **Base URL:** `https://rapi.recombee.com/{databaseId}`
- **Official documentation:** [Insert to Series](https://docs.recombee.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cascadeCreate` | body | `string` | no |
| `itemId` | body | `string` | yes |
| `itemType` | body | `string` | yes |
| `seriesId` | path | `string` | yes |
| `time` | body | `number` | yes |
