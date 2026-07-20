# Create Template with Templated

Creates a new template in Templated.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/template`
- **Base URL:** `https://api.templated.io`
- **Official documentation:** [Create Template](https://templated.io/docs/templates/create/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the template. |
| `width` | body | `number` | yes | The width of the template in pixels. |
| `height` | body | `number` | yes | The height of the template in pixels. |
| `layers[]` | body | `array<object>` | no | Single-page layer definitions for the template. |
| `pages[]` | body | `array<object>` | no | Multi-page definitions for the template. |
| `duration` | body | `number` | no | Default video duration in milliseconds for MP4 renders. |
