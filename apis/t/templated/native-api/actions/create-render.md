# Create Render with Templated

Creates a new render in Templated.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/render`
- **Base URL:** `https://api.templated.io`
- **Official documentation:** [Create Render](https://templated.io/docs/renders/create/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template` | body | `string` | no | The template id that you want to render. |
| `templates[]` | body | `array<string>` | no | Optional list of template ids for batch rendering. |
| `layers` | body | `object` | no | An object of layers that will be updated in the template. |
| `pages[]` | body | `array<object>` | no | Optional page-specific layer modifications for multi-page templates. |
| `format` | body | `string` | no | Render format: jpg, png, webp, pdf, or mp4. |
| `external_id` | body | `string` | no | External identifier to associate the render with an entity in your system. |
| `webhook_url` | body | `string` | no | URL to POST the full render object to when rendering completes. |
| `async` | body | `boolean` | no | When true, create the render asynchronously. |
| `merge` | body | `boolean` | no | When true, merge multi-page template renders into a single PDF. |
