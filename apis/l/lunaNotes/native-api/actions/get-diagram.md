# Get Diagram with LunaNotes

Retrieves a diagram from LunaNotes.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/diagrams/:id`
- **Base URL:** `https://api.lunanotes.io`
- **Official documentation:** [Get Diagram](https://lunanotes.io/docs/diagrams/get-v1-diagrams-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The LunaNotes diagram ID. |
| `include` | query | `string` | no | Comma-separated: video. |
