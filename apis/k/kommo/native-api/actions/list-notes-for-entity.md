# List Notes For Entity with Kommo

## Endpoint

- **Method:** `GET`
- **Path:** `/:entity_type/:entity_id/notes`
- **Base URL:** `https://{referer}/api/v4`
- **Official documentation:** [List Notes For Entity](https://developers.kommo.com/reference/notes-by-entity-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_id` | path | `string` | no | Required path parameter for List Notes For Entity. |
| `entity_type` | path | `string` | yes | The entity type segment used in the path. |
| `entity_type` | path | `string` | no | Required path parameter for List Notes For Entity. |
| `entity_id` | path | `number` | yes | The parent entity identifier. |
