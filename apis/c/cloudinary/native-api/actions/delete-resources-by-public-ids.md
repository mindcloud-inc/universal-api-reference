# Delete Resources by Public IDs with Cloudinary

Deletes Cloudinary resources by public IDs.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/resources/:resource_type/:type`
- **Base URL:** `https://api.cloudinary.com/v1_1/{cloudName}`
- **Official documentation:** [Delete Resources by Public IDs](https://cloudinary.com/documentation/admin_api#delete_resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `public_ids[]` | body | `array<string>` | yes | The public IDs to delete. |
| `resource_type` | path | `string` | yes | The Cloudinary resource type, such as image, video, or raw. |
| `type` | path | `string` | yes | The delivery type, such as upload, private, or authenticated. |
