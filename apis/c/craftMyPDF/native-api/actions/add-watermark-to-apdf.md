# Add watermark to a PDF with CraftMyPDF

Adds a watermark to a PDF in CraftMyPDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/add-watermark`
- **Base URL:** `https://api.craftmypdf.com/v1`
- **Official documentation:** [Add watermark to a PDF](https://craftmypdf.com/docs/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `url` | body | `string` | yes |
| `text` | body | `string` | yes |
| `font_size` | body | `number` | no |
| `opacity` | body | `number` | no |
| `rotation` | body | `number` | no |
| `hex_color` | body | `string` | no |
| `font_family` | body | `string` | no |
| `expiration` | body | `number` | no |
| `output_file` | body | `string` | no |
| `cloud_storage` | body | `number` | no |
| `postaction_s3_filekey` | body | `string` | no |
| `postaction_s3_bucket` | body | `string` | no |
