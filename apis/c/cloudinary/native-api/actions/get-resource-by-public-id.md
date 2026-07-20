# Get Resource by Public ID with Cloudinary

Retrieves a Cloudinary resource by public ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/resources/:resource_type/:type/:public_id`
- **Base URL:** `https://api.cloudinary.com/v1_1/{cloudName}`
- **Official documentation:** [Get Resource by Public ID](https://cloudinary.com/documentation/admin_api#details_of_a_single_resource_by_public_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `public_id` | path | `string` | yes | The Cloudinary public ID. |
| `resource_type` | path | `string` | yes | The Cloudinary resource type, such as image, video, or raw. |
| `type` | path | `string` | yes | The delivery type, such as upload, private, or authenticated. |
