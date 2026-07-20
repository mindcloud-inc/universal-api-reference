# Create Image with HTML/CSS to Image app

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/image`
- **Base URL:** `https://hcti.io`
- **Official documentation:** [Create Image](https://docs.htmlcsstoimage.com/getting-started/using-the-api/#creating-an-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | no | HTML markup to render into an image. |
| `css` | body | `string` | no | CSS styles to apply to the HTML or inject into the target URL page. |
| `url` | body | `string` | no | Public URL to screenshot instead of rendering HTML directly. |
| `google_fonts` | body | `string` | no | Google Fonts to load before rendering. |
| `device_scale` | body | `number` | no | Pixel ratio for rendering, from 0.1 to 3. |
| `viewport_width` | body | `number` | no | Viewport width in pixels. |
| `viewport_height` | body | `number` | no | Viewport height in pixels. |
| `selector` | body | `string` | no | CSS selector for the element to capture. |
| `ms_delay` | body | `number` | no | Milliseconds to wait before rendering. |
| `max_wait_ms` | body | `number` | no | Maximum wait time before capture. |
| `render_when_ready` | body | `boolean` | no | Wait for ScreenshotReady() before capture. |
| `full_screen` | body | `boolean` | no | Capture the full scrollable page height. |
| `block_consent_banners` | body | `boolean` | no | Block consent and cookie banners before capture. |
| `color_scheme` | body | `string` | no | Render using light or dark mode. |
| `timezone` | body | `string` | no | IANA timezone to use while rendering. |
| `disable_twemoji` | body | `boolean` | no | Use native emoji fonts instead of Twemoji. |
