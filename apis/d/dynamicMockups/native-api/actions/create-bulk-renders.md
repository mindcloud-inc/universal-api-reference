# Create Bulk Renders with Dynamic Mockups

Creates bulk renders from a Dynamic Mockups collection.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v1/renders/bulk`
- **Base URL:** `https://app.dynamicmockups.com`
- **Official documentation:** [Create Bulk Renders](https://docs.dynamicmockups.com/api-reference/bulk-render-mockups-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_uuid` | body | `string` | yes | UUID of the Dynamic Mockups collection to bulk render. |
| `artworks` | body | `object` | no | JSON object mapping artwork input keys to image URLs or files. |
| `colors` | body | `object` | no | JSON object mapping color input keys to hex color values. |
| `export_label` | body | `string` | no | Optional label returned back in bulk render response. |
| `export_options.image_format` | body | `string` | no | Optional export format: jpg, png, or webp. |
| `export_options.image_size` | body | `number` | no | Optional output width in pixels. |
| `export_options.mode` | body | `string` | no | Optional mode: view or download. |
