# Create PDF from templates with CraftMyPDF

Creates a PDF from templates in CraftMyPDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/create-merge`
- **Base URL:** `https://api.craftmypdf.com/v1`
- **Official documentation:** [Create PDF from templates](https://craftmypdf.com/docs/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `templates[]` | body | `array<object>` | yes |
| `data` | body | `object` | no |
| `export_type` | body | `string` | no |
| `expiration` | body | `number` | no |
| `output_file` | body | `string` | no |
| `paging` | body | `string` | no |
| `cloud_storage` | body | `number` | no |
| `postaction_s3_filekey` | body | `string` | no |
| `postaction_s3_bucket` | body | `string` | no |
| `image_resample_res` | body | `number` | no |
| `resize_images` | body | `boolean` | no |
| `resize_max_width` | body | `number` | no |
| `resize_max_height` | body | `number` | no |
| `resize_format` | body | `string` | no |
