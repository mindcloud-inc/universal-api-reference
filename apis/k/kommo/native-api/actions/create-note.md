# Create Note with Kommo

## Endpoint

- **Method:** `POST`
- **Path:** `/:entity_type/notes`
- **Base URL:** `https://{referer}/api/v4`
- **Official documentation:** [Create Note](https://developers.kommo.com/reference/add-notes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_type` | path | `string` | yes | Entity type. |
| `entity_type` | path | `string` | no | Required path parameter for Create Note. |
| `[].entity_id` | body | `number` | yes | Entity ID. |
| `[].note_type` | body | `string` | yes | Note type. |
| `[].params` | body | `object` | yes | Note params payload. |
