# Submit Improvement with Remove.bg

Creates an improvement submission in Remove.bg.

## Endpoint

- **Method:** `POST`
- **Path:** `/improve`
- **Base URL:** `https://api.remove.bg/v1.0`
- **Official documentation:** [Submit Improvement](https://www.remove.bg/api#api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image_url` | body | `string` | no | Source image URL. Provide exactly one image source. |
| `image_file_b64` | body | `string` | no | Base64-encoded source image. Provide exactly one image source. |
| `image_filename` | body | `string` | no | Filename to use when the submitted image data does not include one. |
| `tag` | body | `string` | no | Group related submissions with a shared tag. |
