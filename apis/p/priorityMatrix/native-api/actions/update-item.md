# Update Item with Priority Matrix

Updates an existing item in Priority Matrix.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/item/:id/`
- **Base URL:** `https://sync.appfluence.com`
- **Official documentation:** [Update Item](https://sync.appfluence.com/api/v1/docs/#!/item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Priority Matrix item ID. |
| `name` | body | `string` | no | Updated item name. |
| `descriptionText` | body | `string` | no | Plain text item notes or description. |
| `quadrant` | body | `number` | no | Priority Matrix quadrant number. |
| `completionPercentage` | body | `number` | no | Completion percentage from 0 to 100. |
