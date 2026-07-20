# Upload Brand Asset Image with Orshot

## Endpoint

- **Method:** `POST`
- **Path:** `/brand-assets/images/add`
- **Base URL:** `https://api.orshot.com/v1`
- **Official documentation:** [Upload Brand Asset Image](https://orshot.com/docs/api-reference/brand-assets-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `string` | yes | Image URL or base64-encoded image string. |
| `fileName` | body | `string` | no | Optional filename for the uploaded image. |
| `fileType` | body | `string` | no | Optional MIME type for the uploaded image. |
