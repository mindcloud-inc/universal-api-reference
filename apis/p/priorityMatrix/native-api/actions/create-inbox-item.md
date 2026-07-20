# Create Inbox Item with Priority Matrix

Creates a new inbox item in Priority Matrix.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/item/`
- **Base URL:** `https://sync.appfluence.com`
- **Official documentation:** [Create Inbox Item](https://sync.appfluence.com/developer/guide/#concrete-examples)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Item name. |
| `descriptionText` | body | `string` | no | Item notes in plain text. |
| `owner` | body | `string` | yes | Owner email address for the item. |
| `quadrant` | body | `number` | no | Quadrant number: 0 top-left, 1 top-right, 2 bottom-left, 3 bottom-right. |
