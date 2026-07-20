# Create Project Item with Priority Matrix

Creates a new item in a Priority Matrix project.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/item/`
- **Base URL:** `https://sync.appfluence.com`
- **Official documentation:** [Create Project Item](https://sync.appfluence.com/developer/guide/#concrete-examples)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Item name. |
| `descriptionText` | body | `string` | no | Item notes in plain text. |
| `owner` | body | `string` | yes | Owner email address for the item. |
| `projects[]` | body | `array<string>` | yes | Project resource URI list, for example /api/v1/project/234/. |
| `quadrant` | body | `number` | yes | Quadrant number: 0 top-left, 1 top-right, 2 bottom-left, 3 bottom-right. |
