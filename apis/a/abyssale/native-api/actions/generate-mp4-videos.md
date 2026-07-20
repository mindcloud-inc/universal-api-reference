# Generate MP4 Videos with Abyssale

Generates MP4 videos asynchronously in Abyssale.

## Endpoint

- **Method:** `POST`
- **Path:** `/async/banner-builder/:design_id/generate`
- **Base URL:** `https://api.abyssale.com`
- **Official documentation:** [Generate MP4 Videos](https://developers.abyssale.com/rest-api/generation/asynchronous-generation/generate-multi-format-videos)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `design_id` | path | `string` | yes |
| `elements` | body | `object` | yes |
| `template_format_names[]` | body | `array<string>` | yes |
| `video` | body | `object` | no |
