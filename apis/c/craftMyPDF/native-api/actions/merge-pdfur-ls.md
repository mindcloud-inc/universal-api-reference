# Merge PDF URLs with CraftMyPDF

Merges PDF files from URLs in CraftMyPDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/merge-pdfs`
- **Base URL:** `https://api.craftmypdf.com/v1`
- **Official documentation:** [Merge PDF URLs](https://craftmypdf.com/docs/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `urls[]` | body | `array<string>` | yes |
| `expiration` | body | `number` | no |
| `output_file` | body | `string` | no |
| `cloud_storage` | body | `number` | no |
| `postaction_s3_filekey` | body | `string` | no |
| `postaction_s3_bucket` | body | `string` | no |
