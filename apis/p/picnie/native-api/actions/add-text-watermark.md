# Add Text Watermark with Picnie

Creates a watermarked image in Picnie using text.

## Endpoint

- **Method:** `POST`
- **Path:** `/add-watermark-text-on-image`
- **Base URL:** `https://picnie.com/api/v1`
- **Official documentation:** [Add Text Watermark](https://documenter.getpostman.com/view/25712226/2s93CGRvy6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image_url` | body | `string` | yes | Image URL to watermark with text. |
| `project_id` | body | `number` | yes | Project ID that will own the watermarked image. |
| `watermark_text` | body | `string` | yes | Text to render as the watermark. |
| `position` | body | `string` | yes | Watermark position such as bottom-right. |
| `font_size` | body | `number` | yes | Font size in pixels. |
| `font_path` | body | `string` | yes | Font path or font filename. |
| `font_color` | body | `string` | yes | Text color in hex. |
| `opacity` | body | `number` | yes | Text opacity between 0.0 and 1.0. |
| `rotation` | body | `number` | yes | Rotation angle in degrees. |
| `padding` | body | `number` | yes | Padding around the watermark in pixels. |
| `background_color` | body | `string` | yes | Background color in hex. |
| `background_opacity` | body | `number` | yes | Background opacity between 0.0 and 1.0. |
