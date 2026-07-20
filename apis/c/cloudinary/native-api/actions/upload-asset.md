# Upload Asset with Cloudinary

Uploads an asset to your Cloudinary account.

## Endpoint

- **Method:** `POST`
- **Path:** `/:resource_type/upload`
- **Base URL:** `https://api.cloudinary.com/v1_1/{cloudName}`
- **Official documentation:** [Upload Asset](https://cloudinary.com/documentation/image_upload_api_reference#upload_method)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `string` | yes | The file to upload, a remote URL, or a data URI. |
| `resource_type` | path | `string` | yes | The Cloudinary resource type, such as image, video, or raw. |
| `public_id` | body | `string` | no | The identifier to assign to the uploaded asset. |
| `asset_folder` | body | `string` | no | The asset folder where the uploaded asset will be placed. |
