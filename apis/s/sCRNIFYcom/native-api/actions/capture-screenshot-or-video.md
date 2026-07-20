# Capture Screenshot or Video with SCRNIFY.com

Captures a screenshot or video with SCRNIFY.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/capture`
- **Base URL:** `https://api.scrnify.com`
- **Official documentation:** [Capture Screenshot or Video](https://scrnify.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | URL of the page to capture. |
| `format` | query | `list` | yes | Output format. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `type` | query | `list` | yes | Capture type. Accepted values: `0`, `1`. |
| `width` | query | `number` | yes | Viewport width in pixels. |
| `height` | query | `number` | no | Viewport height in pixels. |
| `fullPage` | query | `boolean` | no | Capture the full page. |
