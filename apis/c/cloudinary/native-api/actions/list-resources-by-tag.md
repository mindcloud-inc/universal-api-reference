# List Resources by Tag with Cloudinary

Retrieves Cloudinary resources by tag value.

## Endpoint

- **Method:** `GET`
- **Path:** `/resources/:resource_type/tags/:tag`
- **Base URL:** `https://api.cloudinary.com/v1_1/{cloudName}`
- **Official documentation:** [List Resources by Tag](https://cloudinary.com/documentation/admin_api#resources_by_tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resource_type` | path | `string` | yes | The Cloudinary resource type, such as image, video, or raw. |
| `tag` | path | `string` | yes | The tag to filter by. |
