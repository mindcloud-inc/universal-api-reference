# HTML to Image with 1001fx

Converts HTML or a URL into an image.

## Endpoint

- **Method:** `POST`
- **Path:** `/images/html2image`
- **Base URL:** `https://api.1001fx.com`
- **Official documentation:** [HTML to Image](https://1001fx.com/functions/html2image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fullPage` | body | `boolean` | no | Whether to capture the full rendered page. |
| `height` | body | `number` | no | Output height in pixels. |
| `html` | body | `string` | no | HTML source to render. |
| `outputFormat` | body | `string` | yes | Output image format. |
| `replacements[]` | body | `array` | no | Replacement values used before rendering the HTML. |
| `url` | body | `string` | no | URL to render when not passing raw HTML. |
| `width` | body | `number` | no | Output width in pixels. |
