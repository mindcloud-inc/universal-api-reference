# Update Element In List with Zenkit

Updates a custom field in a Zenkit list.

## Endpoint

- **Method:** `PUT`
- **Path:** `/lists/:listId/elements/:elementId`
- **Base URL:** `https://zenkit.com/api/v1`
- **Official documentation:** [Update Element In List](https://app.zenkit.com/docs/api/elements/put-api-v1-lists-listid-elements-elementid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `elementId` | path | `string` | yes | The element id |
| `listId` | path | `string` | yes | The list id |
| `item` | body | `object` | yes | JSON object for the Zenkit field update body. Zenkit runtime currently expects a single object, not an array. |
