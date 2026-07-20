# Create a PDF asynchronously with CraftMyPDF

Creates a PDF asynchronously in CraftMyPDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/create-async`
- **Base URL:** `https://api.craftmypdf.com/v1`
- **Official documentation:** [Create a PDF asynchronously](https://craftmypdf.com/docs/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data` | body | `object` | yes |
| `template_id` | body | `string` | yes |
| `version` | body | `string` | no |
| `expiration` | body | `number` | no |
| `webhook_url` | body | `string` | no |
| `image_resample_res` | body | `number` | no |
| `cloud_storage` | body | `number` | no |
| `postaction_s3_filekey` | body | `string` | no |
| `postaction_s3_bucket` | body | `string` | no |
| `resize_images` | body | `boolean` | no |
| `resize_max_width` | body | `number` | no |
| `resize_max_height` | body | `number` | no |
| `resize_format` | body | `string` | no |
