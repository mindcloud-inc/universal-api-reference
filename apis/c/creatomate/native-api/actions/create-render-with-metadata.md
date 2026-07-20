# Create Render With Metadata with Creatomate

Creates a render with metadata in Creatomate.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/renders`
- **Base URL:** `https://api.creatomate.com`
- **Official documentation:** [Create Render With Metadata](https://creatomate.com/docs/api/reference/create-a-render)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | body | `string` | yes | The ID of the template to render. |
| `metadata` | body | `string` | yes | Metadata string to store with the render. |
| `modifications` | body | `object` | no | A key-value object of template modifications. |
