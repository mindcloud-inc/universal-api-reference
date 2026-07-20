# Add Activity to Item with Salescamp

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/collections/:collectionId/items/:itemId/activities`
- **Base URL:** `https://api.salescamp.app`
- **Official documentation:** [Add Activity to Item](https://developer.salescamp.app/reference/api-reference/activity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Resource ID of the collection |
| `itemId` | path | `string` | yes | Resource ID of the item |
| `action` | body | `string` | yes | Activity type such as meeting |
| `title` | body | `string` | yes | Activity title |
| `description` | body | `string` | no | Activity description |
| `date` | body | `string` | yes | Activity date |
| `time` | body | `string` | yes | Activity time |
