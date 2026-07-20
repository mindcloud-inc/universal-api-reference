# Create a PDF with CraftMyPDF

Creates a PDF document in CraftMyPDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/create`
- **Base URL:** `https://api.craftmypdf.com/v1`
- **Official documentation:** [Create a PDF](https://craftmypdf.com/docs/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `template_id` | body | `string` | yes |
| `data` | body | `object` | yes |
| `load_data_from` | body | `string` | no |
| `version` | body | `string` | no |
| `export_type` | body | `string` | no |
| `expiration` | body | `number` | no |
| `output_file` | body | `string` | no |
| `image_resample_res` | body | `number` | no |
| `direct_download` | body | `number` | no |
| `cloud_storage` | body | `number` | no |
| `password_protected` | body | `boolean` | no |
| `password` | body | `string` | no |
| `postaction_s3_filekey` | body | `string` | no |
| `postaction_s3_bucket` | body | `string` | no |
| `resize_images` | body | `boolean` | no |
| `resize_max_width` | body | `number` | no |
| `resize_max_height` | body | `number` | no |
| `resize_format` | body | `string` | no |
| `paging` | body | `string` | no |
| `pdf_version` | body | `string` | no |
