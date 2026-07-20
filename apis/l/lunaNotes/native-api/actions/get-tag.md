# Get Tag with LunaNotes

Retrieves a tag from LunaNotes.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/tags/:id`
- **Base URL:** `https://api.lunanotes.io`
- **Official documentation:** [Get Tag](https://lunanotes.io/docs/tags/get-v1-tags-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The LunaNotes tag ID. |
| `include` | query | `string` | no | Comma-separated: notes. |
