# Create Mockup Render with Dynamic Mockups

Creates a mockup render in Dynamic Mockups.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v1/renders`
- **Base URL:** `https://app.dynamicmockups.com`
- **Official documentation:** [Create Mockup Render](https://docs.dynamicmockups.com/api-reference/render-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mockup_uuid` | body | `string` | yes | UUID of the mockup template to render. |
| `smart_objects` | body | `list<object>` | yes | JSON array of smart object mappings (uuid + asset/text options). |
| `export_label` | body | `string` | no | Optional label returned back in render response. |
| `export_options.image_format` | body | `string` | no | Optional export format: jpg, png, or webp. |
| `export_options.image_size` | body | `number` | no | Optional output width in pixels. |
| `export_options.mode` | body | `string` | no | Optional mode: view or download. |
