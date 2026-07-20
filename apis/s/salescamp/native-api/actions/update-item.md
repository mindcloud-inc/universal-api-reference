# Update Item with Salescamp

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/collections/:collectionId/items/:itemId`
- **Base URL:** `https://api.salescamp.app`
- **Official documentation:** [Update Item](https://developer.salescamp.app/reference/api-reference/items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Resource ID of the collection |
| `itemId` | path | `string` | yes | Resource ID of the item |
| `name` | body | `string` | no | Item name |
| `email` | body | `string` | no | Item email |
| `phone` | body | `string` | no | Item phone |
| `website` | body | `string` | no | Item website |
| `value` | body | `number` | no | Item value |
| `status` | body | `string` | no | Item status |
