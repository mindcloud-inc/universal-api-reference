# Create Render With Size Constraints with Creatomate

Creates a render with size constraints in Creatomate.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/renders`
- **Base URL:** `https://api.creatomate.com`
- **Official documentation:** [Create Render With Size Constraints](https://creatomate.com/docs/api/reference/create-a-render)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | body | `string` | yes | The ID of the template to render. |
| `max_width` | body | `number` | no | The maximum output width in pixels. |
| `max_height` | body | `number` | no | The maximum output height in pixels. |
| `modifications` | body | `object` | no | A key-value object of template modifications. |
