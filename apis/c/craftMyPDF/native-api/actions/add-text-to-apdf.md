# Add text to a PDF with CraftMyPDF

Adds text to a PDF in CraftMyPDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/add-text-to-pdf`
- **Base URL:** `https://api.craftmypdf.com/v1`
- **Official documentation:** [Add text to a PDF](https://craftmypdf.com/docs/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `url` | body | `string` | yes |
| `textSettings[]` | body | `array<object>` | yes |
| `textSettings[].page_selector` | body | `string` | yes |
| `textSettings[].text` | body | `string` | yes |
| `textSettings[].position` | body | `string` | yes |
| `textSettings[].offset_x` | body | `number` | no |
| `textSettings[].offset_y` | body | `number` | no |
| `textSettings[].font_size` | body | `number` | no |
| `textSettings[].hex_color` | body | `string` | no |
| `textSettings[].font_family` | body | `string` | no |
| `textSettings[].opacity` | body | `number` | no |
| `textSettings[].rotation` | body | `number` | no |
| `expiration` | body | `number` | no |
| `output_file` | body | `string` | no |
| `cloud_storage` | body | `number` | no |
