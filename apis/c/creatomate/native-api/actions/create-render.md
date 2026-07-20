# Create Render with Creatomate

Creates a new render in Creatomate.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/renders`
- **Base URL:** `https://api.creatomate.com`
- **Official documentation:** [Create Render](https://creatomate.com/docs/api/reference/create-a-render)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | body | `string` | no | The ID of the template to render. |
| `modifications` | body | `object` | no | A key-value object of template modifications. |
| `render_scale` | body | `number` | no | The render scale from 0.1 to 10. Default is 1.0. |
| `max_width` | body | `number` | no | The maximum output width in pixels. |
| `max_height` | body | `number` | no | The maximum output height in pixels. |
| `webhook_url` | body | `string` | no | The URL to call when the render completes. |
| `metadata` | body | `string` | no | Optional metadata string to store with the render. |
| `output_format` | body | `string` | no | The RenderScript output format. |
| `width` | body | `number` | no | The output width in pixels for a RenderScript request. |
| `height` | body | `number` | no | The output height in pixels for a RenderScript request. |
| `elements` | body | `object<object>` | no | The RenderScript elements array. |
