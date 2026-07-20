# Generate Printable PDF Batch with Abyssale

Generates printable PDFs asynchronously in Abyssale.

## Endpoint

- **Method:** `POST`
- **Path:** `/async/banner-builder/:design_id/generate`
- **Base URL:** `https://api.abyssale.com`
- **Official documentation:** [Generate Printable PDF Batch](https://developers.abyssale.com/rest-api/generation/asynchronous-generation/generate-multi-format-pdfs-for-printing)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `design_id` | path | `string` | yes |
| `elements` | body | `object` | yes |
| `template_format_names[]` | body | `array<string>` | yes |
| `print` | body | `object` | no |
