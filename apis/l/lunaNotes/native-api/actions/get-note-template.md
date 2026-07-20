# Get Note Template with LunaNotes

Retrieves a note template from LunaNotes.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/note-templates/:id`
- **Base URL:** `https://api.lunanotes.io`
- **Official documentation:** [Get Note Template](https://lunanotes.io/docs/note-templates/get-v1-note-templates-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The LunaNotes note template ID. |
| `include` | query | `string` | no | Include the related system template in the response |
