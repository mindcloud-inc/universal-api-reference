# Render Multiple Mockups with Dynamic Mockups

Creates multiple mockup renders in Dynamic Mockups.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v1/renders/batch`
- **Base URL:** `https://app.dynamicmockups.com`
- **Official documentation:** [Render Multiple Mockups](https://docs.dynamicmockups.com/api-reference/batch-render-mockups-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `renders` | body | `list<object>` | yes | JSON array of render objects. Each item requires mockup_uuid and smart_objects. |
| `export_options.image_format` | body | `string` | no | Optional export format applied to all renders: jpg, png, or webp. |
| `export_options.image_size` | body | `number` | no | Optional output width in pixels for all renders. |
| `export_options.mode` | body | `string` | no | Optional mode for all renders: view or download. |
