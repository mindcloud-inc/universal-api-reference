# Create Image with API Template

Creates an image in API Template.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/create-image`
- **Base URL:** `https://rest.apitemplate.io`
- **Official documentation:** [Create Image](https://apitemplate.io/apiv2/#tag/API-Integration/operation/create-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | query | `string` | yes | Template ID to render. |
| `output_image_type` | query | `string` | no | Return JPEG, PNG, or both. |
| `expiration` | query | `number` | no | Minutes before the generated file expires; use 0 to store permanently. |
| `cloud_storage` | query | `number` | no | Whether to upload the generated file to APITemplate cloud storage. |
| `meta` | query | `string` | no | Optional metadata string to attach to the job. |
| `overrides[]` | body | `array<object>` | no | Array of object overrides to apply to the image template. |
