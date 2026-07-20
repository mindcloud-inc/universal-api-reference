# Create Render With Template Modifications with Creatomate

Creates a render with template modifications in Creatomate.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/renders`
- **Base URL:** `https://api.creatomate.com`
- **Official documentation:** [Create Render With Template Modifications](https://creatomate.com/docs/fundamentals/getting-started/template-modifications)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | body | `string` | yes | The ID of the template to render. |
| `modifications` | body | `object` | yes | A key-value object of template modifications. |
