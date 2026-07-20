# Add Item Property with Recombee

Creates a new item property in Recombee.

## Endpoint

- **Method:** `PUT`
- **Path:** `/items/properties/:propertyName`
- **Base URL:** `https://rapi.recombee.com/{databaseId}`
- **Official documentation:** [Add Item Property](https://docs.recombee.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `propertyName` | path | `string` | yes |
| `type` | query | `string` | yes |
