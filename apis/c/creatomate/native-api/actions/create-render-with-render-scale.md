# Create Render With Render Scale with Creatomate

Creates a render with render scale in Creatomate.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/renders`
- **Base URL:** `https://api.creatomate.com`
- **Official documentation:** [Create Render With Render Scale](https://creatomate.com/docs/api/reference/create-a-render)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | body | `string` | yes | The ID of the template to render. |
| `render_scale` | body | `number` | yes | The render scale from 0.1 to 10. Default is 1.0. |
| `modifications` | body | `object` | no | A key-value object of template modifications. |
