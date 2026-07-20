# Create Screenshot from HTML with PeekShot

Creates a screenshot from HTML in PeekShot.

## Endpoint

- **Method:** `POST`
- **Path:** `/html-to-image`
- **Base URL:** `https://api.peekshot.com/api/v1`
- **Official documentation:** [Create Screenshot from HTML](https://docs.peekshot.com/api-reference/html-to-screenshot-hpie)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | Unique project identifier. |
| `html` | body | `string` | yes | HTML content to capture. |
| `width` | body | `string` | no | Screenshot width. Docs default: 1280. |
| `height` | body | `string` | no | Screenshot height. Docs default: 1024. |
| `file_type` | body | `string` | no | Output format: jpeg, png, webp, or avif. |
| `delay` | body | `string` | no | Time in seconds to wait before capturing. |
| `full_page` | body | `string` | no | Capture the full page instead of only the viewport. |
| `emulate_device` | body | `string` | no | Render the HTML using a supported device profile. |
| `retina` | body | `string` | no | Use true for higher-resolution screenshots. |
