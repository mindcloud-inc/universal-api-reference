# Update Model with Fish Audio

Updates an existing voice model in Fish Audio.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/model/:id`
- **Base URL:** `https://api.fish.audio`
- **Official documentation:** [Update Model](https://docs.fish.audio/api-reference/endpoint/model/update-model)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Fish Audio model ID. |
| `title` | body | `string` | no | Updated model title. |
| `description` | body | `string` | no | Updated model description. |
| `cover_image` | body | `file` | no | Updated model cover image. |
| `visibility` | body | `list` | no | Updated model visibility. Accepted values: `0`, `1`, `2`. |
| `tags[]` | body | `array<string>` | no | Updated model tags. |
