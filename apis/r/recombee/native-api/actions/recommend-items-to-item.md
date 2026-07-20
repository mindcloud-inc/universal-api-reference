# Recommend Items to Item with Recombee

Retrieves item recommendations for an item from Recombee.

## Endpoint

- **Method:** `POST`
- **Path:** `/recomms/items/:itemId/items/`
- **Base URL:** `https://rapi.recombee.com/{databaseId}`
- **Official documentation:** [Recommend Items to Item](https://docs.recombee.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `count` | body | `string` | no |
| `itemId` | path | `string` | yes |
| `targetUserId` | body | `string` | yes |
