# Delete Asset with Cloudinary

Deletes an asset from your Cloudinary account.

## Endpoint

- **Method:** `POST`
- **Path:** `/:resource_type/destroy`
- **Base URL:** `https://api.cloudinary.com/v1_1/{cloudName}`
- **Official documentation:** [Delete Asset](https://cloudinary.com/documentation/image_upload_api_reference#destroy_method)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `public_id` | body | `string` | yes | The public ID to destroy. |
| `resource_type` | path | `string` | yes | The Cloudinary resource type, such as image, video, or raw. |
