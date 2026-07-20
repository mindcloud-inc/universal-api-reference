# List Tags with Cloudinary

Retrieves tags from your Cloudinary account.

## Endpoint

- **Method:** `GET`
- **Path:** `/tags/:resource_type`
- **Base URL:** `https://api.cloudinary.com/v1_1/{cloudName}`
- **Official documentation:** [List Tags](https://cloudinary.com/documentation/admin_api#tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resource_type` | path | `string` | yes | The Cloudinary resource type, such as image, video, or raw. |
