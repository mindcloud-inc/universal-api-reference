# Update Item with Qlik

Updates an existing item in Qlik.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/items/:itemId`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Update Item](https://qlik.dev/apis/rest/items/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemId` | path | `string` | yes | Qlik item ID. |
| `resourceType` | body | `string` | yes | Qlik item resource type. |
| `name` | body | `string` | no | Item name. |
| `spaceId` | body | `string` | no | Space ID for the item. |
