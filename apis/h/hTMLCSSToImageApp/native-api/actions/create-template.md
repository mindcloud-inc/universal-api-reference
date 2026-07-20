# Create Template with HTML/CSS to Image app

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/template`
- **Base URL:** `https://hcti.io`
- **Official documentation:** [Create Template](https://docs.htmlcsstoimage.com/getting-started/templates/#creating-a-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | yes | HTML markup to save in the template. |
| `css` | body | `string` | no | CSS styles for the template. |
| `name` | body | `string` | no | Short name for the template. |
| `description` | body | `string` | no | Optional description for the template. |
| `google_fonts` | body | `string` | no | Google Fonts to load before rendering the template. |
| `selector` | body | `string` | no | CSS selector for the element to capture. |
| `ms_delay` | body | `number` | no | Milliseconds to wait before rendering. |
| `max_wait_ms` | body | `number` | no | Maximum wait time before capture. |
| `device_scale` | body | `number` | no | Pixel ratio for rendering, from 0.1 to 3. |
| `render_when_ready` | body | `boolean` | no | Wait for ScreenshotReady() before capture. |
| `viewport_width` | body | `number` | no | Viewport width in pixels. |
| `viewport_height` | body | `number` | no | Viewport height in pixels. |
| `color_scheme` | body | `string` | no | Render using light or dark mode. |
| `timezone` | body | `string` | no | IANA timezone to use while rendering. |
| `disable_twemoji` | body | `boolean` | no | Use native emoji fonts instead of Twemoji. |
