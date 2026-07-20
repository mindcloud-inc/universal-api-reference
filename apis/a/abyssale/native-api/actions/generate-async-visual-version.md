# Generate Async Visual Version with Abyssale

Generates a visual variation asynchronously in Abyssale.

## Endpoint

- **Method:** `POST`
- **Path:** `/async/banner-builder/:design_id/generate`
- **Base URL:** `https://api.abyssale.com`
- **Official documentation:** [Generate Async Visual Version](https://developers.abyssale.com/rest-api/generation/visual-versioning)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `design_id` | path | `string` | yes |
| `original_visual_id` | body | `string` | yes |
| `elements` | body | `object` | yes |
| `template_format_names[]` | body | `array<string>` | yes |
