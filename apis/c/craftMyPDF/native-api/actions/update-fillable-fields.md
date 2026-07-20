# Update fillable fields with CraftMyPDF

Updates fillable PDF fields in CraftMyPDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/update-pdf-fields`
- **Base URL:** `https://api.craftmypdf.com/v1`
- **Official documentation:** [Update fillable fields](https://craftmypdf.com/docs/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `url` | body | `string` | yes |
| `fields[]` | body | `array<object>` | yes |
| `fields[].id` | body | `string` | no |
| `fields[].value` | body | `string` | no |
| `fields[].readOnly` | body | `boolean` | no |
| `fields[].fontSize` | body | `number` | no |
| `expiration` | body | `number` | no |
| `output_file` | body | `string` | no |
| `cloud_storage` | body | `number` | no |
