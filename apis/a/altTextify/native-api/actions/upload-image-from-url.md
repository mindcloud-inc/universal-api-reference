# Upload Image From URL with AltTextify

Creates a new image in AltTextify from an image URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/image/url`
- **Base URL:** `https://api.alttextify.net/api/v1`
- **Official documentation:** [Upload Image From URL](https://apidoc.alttextify.net/#api-Image-UploadImageURL)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `string` | yes | The public URL of the image to upload. |
| `lang` | body | `string` | yes | Language code for generated alt text. |
| `max_chars` | body | `number` | yes | Maximum length of the generated alt text. |
