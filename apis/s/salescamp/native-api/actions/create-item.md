# Create Item with Salescamp

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/collections/:collectionId/items`
- **Base URL:** `https://api.salescamp.app`
- **Official documentation:** [Create Item](https://developer.salescamp.app/reference/api-reference/items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Resource ID of the collection |
| `name` | body | `string` | yes | Item name |
| `email` | body | `string` | no | Item email |
| `phone` | body | `string` | no | Item phone |
| `website` | body | `string` | no | Item website |
| `value` | body | `number` | no | Item value |
| `status` | body | `string` | no | Item status |
