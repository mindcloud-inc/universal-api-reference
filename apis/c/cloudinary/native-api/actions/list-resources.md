# List Resources with Cloudinary

Retrieves resources from your Cloudinary account.

## Endpoint

- **Method:** `GET`
- **Path:** `/resources/:resource_type/:type`
- **Base URL:** `https://api.cloudinary.com/v1_1/{cloudName}`
- **Official documentation:** [List Resources](https://cloudinary.com/documentation/admin_api#resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resource_type` | path | `string` | yes | The Cloudinary resource type, such as image, video, or raw. |
| `type` | path | `string` | yes | The delivery type, such as upload, private, or authenticated. |
