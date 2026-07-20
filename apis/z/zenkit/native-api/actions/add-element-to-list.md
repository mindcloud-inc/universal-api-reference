# Add Element To List with Zenkit

Creates a custom field in a Zenkit list.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/:listId/elements`
- **Base URL:** `https://zenkit.com/api/v1`
- **Official documentation:** [Add Element To List](https://app.zenkit.com/docs/api/elements/post-api-v1-lists-listid-elements)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | The list id |
| `items` | body | `object` | yes | JSON array of Zenkit field definitions. Zenkit runtime currently requires lowercase `elementcategory` in each object. |
