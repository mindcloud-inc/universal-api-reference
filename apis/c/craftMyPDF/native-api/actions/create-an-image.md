# Create an image with CraftMyPDF

Creates an image file in CraftMyPDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/create-image`
- **Base URL:** `https://api.craftmypdf.com/v1`
- **Official documentation:** [Create an image](https://craftmypdf.com/docs/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data` | body | `object` | yes |
| `load_data_from` | body | `string` | no |
| `template_id` | body | `string` | yes |
| `version` | body | `string` | no |
| `export_type` | body | `string` | no |
| `expiration` | body | `number` | no |
| `output_file` | body | `string` | no |
| `output_type` | body | `string` | no |
| `cloud_storage` | body | `number` | no |
| `postaction_s3_filekey` | body | `string` | no |
| `postaction_s3_bucket` | body | `string` | no |
