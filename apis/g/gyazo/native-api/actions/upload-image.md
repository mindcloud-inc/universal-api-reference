# Upload Image with Gyazo

Uploads a new image to Gyazo.

## Endpoint

- **Method:** `POST`
- **Path:** `https://upload.gyazo.com/api/upload`
- **Base URL:** `https://api.gyazo.com`
- **Official documentation:** [Upload Image](https://gyazo.com/api/docs/image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `imagedata` | body | `string` | yes | Binary image data sent as multipart/form-data. Include a filename in the multipart part. |
| `access_policy` | body | `string` | no | Image visibility. Gyazo documents anyone or only_me. Accepted values: `0`, `1`. |
| `metadata_is_public` | body | `string` | no | Whether page title and URL metadata should be public. Accepted values: `0`, `1`. |
| `referer_url` | body | `string` | no | Referer site URL. |
| `app` | body | `string` | no | Application name attached to the upload metadata. |
| `title` | body | `string` | no | Site title metadata. |
| `desc` | body | `string` | no | Comment or description attached to the image. |
| `created_at` | body | `number` | no | Image creation time as a Unix timestamp. |
| `collection_id` | body | `string` | no | Collection identifier to add the image into. |
