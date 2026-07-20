# Generate HTML5 Banner Ads with Abyssale

Generates HTML5 banner ads asynchronously in Abyssale.

## Endpoint

- **Method:** `POST`
- **Path:** `/async/banner-builder/:design_id/generate`
- **Base URL:** `https://api.abyssale.com`
- **Official documentation:** [Generate HTML5 Banner Ads](https://developers.abyssale.com/rest-api/generation/asynchronous-generation/generate-html5-banner-ads)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `design_id` | path | `string` | yes |
| `elements` | body | `object` | yes |
| `template_format_names[]` | body | `array<string>` | yes |
| `html5` | body | `object` | no |
