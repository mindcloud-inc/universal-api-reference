# Set Item Values with Recombee

Updates values for an item in Recombee.

## Endpoint

- **Method:** `POST`
- **Path:** `/items/:itemId`
- **Base URL:** `https://rapi.recombee.com/{databaseId}`
- **Official documentation:** [Set Item Values](https://docs.recombee.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cascadeCreate` | query | `string` | no |
| `itemId` | path | `string` | yes |
| `values` | body | `object` | yes |
