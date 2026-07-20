# Upload Raw Image with AltTextify

Creates a new image in AltTextify from base64 image data.

## Endpoint

- **Method:** `POST`
- **Path:** `/image/raw`
- **Base URL:** `https://api.alttextify.net/api/v1`
- **Official documentation:** [Upload Raw Image](https://apidoc.alttextify.net/#api-Image-UploadRawImage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `string` | yes | A base64-encoded image payload, preferably with a data URI prefix. |
| `lang` | body | `string` | yes | Language code for generated alt text. |
| `max_chars` | body | `number` | yes | Maximum length of the generated alt text. |
