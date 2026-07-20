# Create Render with Clipcat

Creates a new video render request in Clipcat.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/renders`
- **Base URL:** `https://api.clipcat.com`
- **Official documentation:** [Create Render](https://developers.clipcat.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `metadata` | body | `string` | no | Optional metadata to store with the render. |
| `modifications[]` | body | `array<object>` | yes | A JSON array of render modifications. Each item can include scene, object, text, color, font-family, background-image, background-color, border-color, border-width, or media_url. |
| `template` | body | `string` | yes | The template UID to render. |
| `webhook_url` | body | `string` | no | Optional webhook URL that receives the finished render object. |
