# Render Custom HTML with ScreenshotAPI

Creates a screenshot from custom HTML in ScreenshotAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/screenshot`
- **Base URL:** `https://shot.screenshotapi.net/v3`
- **Official documentation:** [Render Custom HTML](https://www.screenshotapi.net/docs/renderScreenshot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_html` | query | `string` | yes | HTML markup to render instead of loading a URL. |
| `file_type` | query | `string` | no | The file format to generate from the provided HTML. |
| `fresh` | query | `boolean` | no | Request a newly rendered custom HTML capture instead of cached output. |
