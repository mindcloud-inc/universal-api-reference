# Update Item Notes with Priority Matrix

Updates item notes in Priority Matrix.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/item/:id/`
- **Base URL:** `https://sync.appfluence.com`
- **Official documentation:** [Update Item Notes](https://sync.appfluence.com/api/v1/docs/#!/item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Priority Matrix item ID. |
| `descriptionText` | body | `string` | yes | Plain text item notes. |
