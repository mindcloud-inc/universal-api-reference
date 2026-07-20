# Get Rendered Images with Figma

Retrieves rendered images from a Figma file.

## Endpoint

- **Method:** `GET`
- **Path:** `/images/:key`
- **Base URL:** `https://api.figma.com/v1`
- **Official documentation:** [Get Rendered Images](https://developers.figma.com/docs/rest-api/file-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | Key of the file to render images from. |
| `ids` | query | `string` | yes | Comma-separated node IDs to render. |
| `version` | query | `string` | no | Version ID to render from. |
| `scale` | query | `number` | no | Scale factor for rendered images. |
| `format` | query | `string` | no | Image format to render (jpg, png, svg, pdf). |
| `svg_outline_text` | query | `boolean` | no | Whether to outline text in SVG output. |
| `svg_include_id` | query | `boolean` | no | Whether to include IDs in SVG output. |
| `svg_include_node_id` | query | `boolean` | no | Whether to include node IDs in SVG output. |
| `svg_simplify_stroke` | query | `boolean` | no | Whether to simplify stroke geometry in SVG output. |
| `contents_only` | query | `boolean` | no | Whether to render only node contents without effects. |
| `use_absolute_bounds` | query | `boolean` | no | Whether to use absolute bounds for rendering. |
