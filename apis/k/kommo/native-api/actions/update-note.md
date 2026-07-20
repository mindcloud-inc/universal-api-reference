# Update Note with Kommo

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:entity_type/notes/:id`
- **Base URL:** `https://{referer}/api/v4`
- **Official documentation:** [Update Note](https://developers.kommo.com/reference/edit-note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_type` | path | `string` | yes | Entity type. |
| `entity_type` | path | `string` | no | Required path parameter for Update Note. |
| `id` | path | `number` | yes | Note ID. |
| `entity_id` | body | `number` | yes | Entity ID. |
| `note_type` | body | `string` | yes | Note type. |
| `params` | body | `object` | yes | Note params payload. |
