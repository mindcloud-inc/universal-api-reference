# Apply Explicit Asset Actions with Cloudinary

Applies explicit asset actions in Cloudinary.

## Endpoint

- **Method:** `POST`
- **Path:** `/:resource_type/explicit`
- **Base URL:** `https://api.cloudinary.com/v1_1/{cloudName}`
- **Official documentation:** [Apply Explicit Asset Actions](https://cloudinary.com/documentation/image_upload_api_reference#explicit_method)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `public_id` | body | `string` | yes | The public ID of the existing asset. |
| `resource_type` | path | `string` | yes | The Cloudinary resource type, such as image, video, or raw. |
| `type` | body | `string` | yes | The delivery type, such as upload, private, or authenticated. |
| `tags` | body | `string` | no | A comma-separated list of tags to assign to the asset. |
