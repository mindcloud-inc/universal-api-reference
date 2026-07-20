# Create Render From RenderScript with Creatomate

Creates a render from RenderScript in Creatomate.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/renders`
- **Base URL:** `https://api.creatomate.com`
- **Official documentation:** [Create Render From RenderScript](https://creatomate.com/docs/api/quick-start/create-a-video-by-render-script)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `output_format` | body | `string` | yes | The RenderScript output format. |
| `width` | body | `number` | yes | The output width in pixels. |
| `height` | body | `number` | yes | The output height in pixels. |
| `elements` | body | `object<object>` | yes | The RenderScript elements array. |
