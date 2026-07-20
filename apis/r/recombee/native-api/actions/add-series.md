# Add Series with Recombee

Creates a new series in Recombee.

## Endpoint

- **Method:** `PUT`
- **Path:** `/series/:seriesId`
- **Base URL:** `https://rapi.recombee.com/{databaseId}`
- **Official documentation:** [Add Series](https://docs.recombee.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cascadeCreate` | body | `string` | no |
| `seriesId` | path | `string` | yes |
