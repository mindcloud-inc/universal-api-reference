# Rename Asset with Cloudinary

Renames an asset in your Cloudinary account.

## Endpoint

- **Method:** `POST`
- **Path:** `/:resource_type/rename`
- **Base URL:** `https://api.cloudinary.com/v1_1/{cloudName}`
- **Official documentation:** [Rename Asset](https://cloudinary.com/documentation/image_upload_api_reference#rename_method)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_public_id` | body | `string` | yes | The current public ID. |
| `resource_type` | path | `string` | yes | The Cloudinary resource type, such as image, video, or raw. |
| `to_public_id` | body | `string` | yes | The new public ID. |
