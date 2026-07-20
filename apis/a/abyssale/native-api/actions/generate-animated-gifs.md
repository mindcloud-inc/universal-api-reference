# Generate Animated GIFs with Abyssale

Generates animated GIFs asynchronously in Abyssale.

## Endpoint

- **Method:** `POST`
- **Path:** `/async/banner-builder/:design_id/generate`
- **Base URL:** `https://api.abyssale.com`
- **Official documentation:** [Generate Animated GIFs](https://developers.abyssale.com/rest-api/generation/asynchronous-generation/generate-multi-format-animated-gifs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `design_id` | path | `string` | yes |
| `elements` | body | `object` | yes |
| `template_format_names[]` | body | `array<string>` | yes |
| `gif` | body | `object` | no |
